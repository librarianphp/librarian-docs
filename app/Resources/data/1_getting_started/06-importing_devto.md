---
title: Importing Posts from DEV.to
published: true
description: How to Import your posts from dev.to with Librarian
---

To import DEV posts, first edit the `config.php` file to include your own DEV username, then run:

```command
php librarian import:devto
```

This will import all your published posts on the DEV.to platform. Once the import is finished, you can reload your main page and you should see all posts listed within your blog.