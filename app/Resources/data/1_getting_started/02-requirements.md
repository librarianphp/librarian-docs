---
title: Requirements
published: true
description: Requirements to install and run Librarian
---

To run Librarian locally on a development environment, you'll need:

- PHP 7.4+ (`cli` is enough for developing with the built-in PHP web server)
- [Composer](https://getcomposer.org)
- [NPM](https://docs.npmjs.com/cli/v7) (recommended due to Tailwind, but only required if you're modifying templates)

Librarian uses [Tailwind css](https://tailwindcss.com/docs) for its front-end, but the main `app.css` is included in the `web` public directory to facilitate usage.
You are only required to run `npm` if you make significant changes to the layout, or if you want to include additional CSS in the assets build pipeline.