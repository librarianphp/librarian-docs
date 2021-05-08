---
title: Introduction
published: true
description: About Librarian
---

Librarian is a stateless CMS based on static files. It uses the same format as DEV.to for markdown files with a front matter and liquid tags for custom functionality.
The front matter is fluid and doesn't have a fixed spec, meaning you can include any custom fields you want and fetch them from your templates.

Librarian doesn't use databases, sessions, or users. Administration is made from the command-line.
For multiple authors, author information must be defined as metadata within the front matter.

This is an experimental project built to keep content decoupled from the application itself, while keeping a very low footprint and functioning as a middle ground between static sites and dynamic CMSs.

Liquid tags supported at the moment:

* {% audio path_to_mp3.mp3 %} (embeds mp3 audio)
* {% video path_to_mp4.mp4 %} (embeds mp4 video)
* {% twitter tweet_id %} (embeds a Tweet)
* {% youtube video_ID %} (embeds a YouTube video)
* {% github file_url %} (embeds a Gist or a Repository File)

Librarian **is not** a static site generator, and the idea is to provide a mix of static files and dynamic capabilities that don't require sessions or databases.
It facilitates contributing via GitHub, so it's great for documentation in general.

## Requirements

To run Librarian locally on a development environment, you'll need:

- PHP 7.4+ (`cli` is all we need)
- [Composer](https://getcomposer.org)
- [NPM](https://docs.npmjs.com/cli/v7) (recommended due to Tailwind, but only required if you're modifying templates)

Librarian uses [Tailwind css](https://tailwindcss.com/docs) for its front-end, but the main `app.css` is included in the `web` public directory to facilitate usage.
You are only required to run `npm` if you make significant changes to the layout.