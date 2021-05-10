---
title: Using Markdown
published: true
description: Librarian uses markdown extra. Here you can find a quick reference for the most common tags.
---

Here you can find a quick reference for the most commonly used Markdown tags and how they are rendered within Librarian views.

## Headers

```markdown
# H1 Header
## H2 Header
### H3 Header
```

## Text Formatting

| Style | Code | Example |
|------|---------|-------------|
| Italic | `*text*` | *text* |
| Bold | `**text**` | **text** |
| Combined | `*testing **bold** now*` | *testing **bold** now*| 
| Strikethrough | `~~text~~` | ~~text~~| 

## Links

```markdown
[link description](link-URL)
```
## Images

```markdown
![image caption](image-path-or-URL)
```
## Lists

Unordered lists:

```markdown
- unordered list item 1
  - second level
    - third level
- unordered list item 2
- unordered list item 3
- unordered list item 4
```
Result:

- unordered list item 1
    - second level
        - third level
- unordered list item 2
- unordered list item 3
- unordered list item 4

Ordered (numbered) lists:

```markdown
1. ordered list item 1
2. second level
5. numbers are rendered in order, doesn't matter how you index the items
```
Result:

1. ordered list item 1
2. second level
5. numbers are rendered in order, doesn't matter how you index the items

## Formatting Code 

You can use code blocks or inline code tags to better render code with Librarian. Syntax highlighting is supported via Prism.

### Code Blocks

Code blocks start and finish with three backticks (```) and support multiple languages, for instance consider a block such as:


<pre>
```php
</pre>
```
<?php

class Test
{
  public $property = "value";
  
  function __construct($var)
  {
    $this->property = $var;
  }
}

```
<pre>
```
</pre>

Will render like this:

```php
<?php

class Test
{
  public $property = "value";
  
  function __construct($var)
  {
    $this->property = $var;
  }
}
```

### Inline Code

When you want to refer to a command or a small piece of code within a sentence, you can use inline code.

```markdown
this is `inline code`
```
Result:

this is `inline code`

Librarian uses Prism for code highlighting.


## Tables

```markdown
| Title 1 | Title 2 | Title 3 |
|---------|---------|---------|
| Row 1x1 | Row 1x2 | Row 1x3 |
| Row 2x1 | Row 2x2 | Row 2x3 |
| Row 3x1 | Row 3x2 | Row 3x3 |
```
Result:

| Title 1 | Title 2 | Title 3 |
|---------|---------|---------|
| Row 1x1 | Row 1x2 | Row 1x3 |
| Row 2x1 | Row 2x2 | Row 2x3 |
| Row 3x1 | Row 3x2 | Row 3x3 |


