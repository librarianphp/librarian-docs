---
title: Librarian Liquid Tags
published: true
description: 
---

Librarian uses liquid tags to offer extended and customizable embeds in markdown, inspired by DEV.to.

Currently, we have a limited number of liquid tags implemented, but this collection is expected to grow in the future (contributions are welcome).



```
data/
  posts/
    - 01-my-post-title.md
    - 02-another-post.md
  pages/
    - about.md
    - sponsors.md
```

This data structure yields the following URLs:

```
/pages
/pages/about
/pages/sponsors
/posts
/posts/01-my-post-title
/posts/02-another-post
```