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

| Tag | Example | Description |
|-----|---------|-------------|
| `youtube` | `{% audio path_to_mp3.mp3 %}` | embeds mp3 audio |
| `video` | `{% video path_to_mp4.mp4 %}` | embeds mp4 video |
| `tweet_id` | `{% twitter tweet_id %}` | embeds a Tweet |
| `youtube` | `{% youtube video_ID %}` | embeds a YouTube video |
| `github` | `{% github file_url %}` | embeds a Gist or a Repository File |

Librarian **is not** a static site generator, and the idea is to provide a mix of static files and dynamic capabilities that don't require sessions or databases.
It facilitates contributing via GitHub, so it's great for documentation in general.