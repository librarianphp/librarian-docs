---
title: Bootstrapping a New Librarian Application
published: true
description: How to create a new librarian Application using Composer.
---

To get started with Librarian, first you'll need to bootstrap a new application using [Composer](https://getcomposer.org).

From your development machine, where you have PHP and Composer installed, run:

```command
composer create-project librarianphp/librarian myblog
```

Once the dependencies are installed, you can run Librarian with the built-in PHP server:

```command
cd myblog
php -S 0.0.0.0:8000 -t web/
```

Then you can access the app from your browser at `http://localhost:8000`. You'll see a page like this:

![Librarian Default Page](/img/librarian_default_page.png)
