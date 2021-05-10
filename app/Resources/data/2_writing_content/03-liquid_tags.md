---
title: Librarian Liquid Tags
published: true
description: 
---

Librarian uses liquid tags to offer extended and customizable embeds in markdown, inspired by DEV.to.

Currently, we have a limited number of liquid tags implemented, but this collection is expected to grow in the future (contributions are welcome).


Liquid tags supported at the moment:

| Tag | Example | Description |
|-----|---------|-------------|
| `youtube` | `{% audio path_to_mp3.mp3 %}` | embeds mp3 audio |
| `video` | `{% video path_to_mp4.mp4 %}` | embeds mp4 video |
| `tweet_id` | `{% twitter tweet_id %}` | embeds a Tweet |
| `youtube` | `{% youtube video_ID %}` | embeds a YouTube video |
| `github` | `{% github file_url %}` | embeds a Gist or a Repository File |