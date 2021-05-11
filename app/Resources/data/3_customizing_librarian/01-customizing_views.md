---
title: Customizing Librarian Views
published: true
description: How to use Librarian Themes
---

Librarian uses [Twig](https://twig.symfony.com/), the Symfony template engine, to deliver front-end views. 

Templates are organized into themes. To customize your views, it is best to create a custom theme based on the theme you want to be the base for your custom design.
To do that, create a copy of the theme folder in `app/Resources/themes` and change the `templates_path` in your `config.php` file to point to your custom theme folder.  

The default themes are built with [Tailwind CSS](https://tailwindcss.com/). A `tailwind.config.js` is included in the root of the project, as well as the `package.json` file to set up NPM dependencies (required if you're rebuilding the CSS assets).


Librarian comes with a default blog style theme. You can find more themes at [librarianphp/librarian-themes](https://github.com/librarianphp/librarian-themes). 

Theme contributions welcome!
