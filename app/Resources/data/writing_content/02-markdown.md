---
title: Librarian's Markdown
published: true
description: 
---

Librarian uses a two-level structure where directories inside its `data` dir are indexed as content types or categories, and the content inside each of these directories is indexed as entries in those categories.
Consider the following structure:

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