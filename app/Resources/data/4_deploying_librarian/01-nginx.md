---
title: Nginx + PHP-FPM Configuration
published: true
description: In this page you can find an example configuration to deploy Librarian within Nginx servers.
---

To deploy Librarian within Nginx, you'll need to also install PHP-FPM on the server (MySQL not needed!). Check out this [LEMP tutorial](https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-on-ubuntu-20-04) for details on how to get these installed - you can skip the MySQL step(s).

This is an example of functional Nginx configuration to host a Librarian website with PHP-FPM (PHP 7.4):

```
server {
    listen 80;
    server_name domain_name www.domain_name;
    root /var/www/librarian-website;

    add_header X-Frame-Options "SAMEORIGIN";
    add_header X-XSS-Protection "1; mode=block";
    add_header X-Content-Type-Options "nosniff";

    index index.html index.htm index.php;

    charset utf-8;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location = /favicon.ico { access_log off; log_not_found off; }
    location = /robots.txt  { access_log off; log_not_found off; }

    error_page 404 /index.php;

    location ~ \.php$ {
        fastcgi_pass unix:/var/run/php/php7.4-fpm.sock;
        fastcgi_index index.php;
        fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
        include fastcgi_params;
    }

    location ~ /\.(?!well-known).* {
        deny all;
    }
}
```