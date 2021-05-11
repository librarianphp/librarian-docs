---
title: Creating Custom Liquid Tags
published: true
description: How to create custom liquid tags
---

To parse markdown, front matter, and liquid tags, Librarian uses [Parsed](https://github.com/librarianphp/parsed), a generic content parser library that supports the format used by [DEV / Forem](https://dev.to). 
Parsed was built-in in the first versions of Librarian, but we have moved this implementation to a standalone package (available as `librarianphp/parsed` on Packagist) so that it can be used within systems other than Librarian.

Parsed comes with [a few basic liquid tags](/2_writing_content/03-liquid_tags) already implemented, but it offers support for creating your own custom liquid tags, which is the actual exciting part.

Liquid tags are classes that implement the `CustomTagParserInterface`. They need to implement a method named `parse`, which receives the string provided to the liquid tag when called from the markdown file.
For instance, this is the full code for the `video` liquid tag parser class:

```php
<?php
#app/CustomTagParser/VideoTagParser.php

namespace Parsed\CustomTagParser;

use Parsed\CustomTagParserInterface;

class VideoTagParser implements CustomTagParserInterface
{
    public function parse($tag_value, array $params = [])
    {
        return "<video controls>" .
         "<source src=\"$tag_value\" type=\"video/mp4\">" .
         "Your browser does not support the video tag." .
         "</video>";
    }
}
```

You'll have to include your custom tag parser class within the ContentParser, and this must be done at the application entry point `web/index.php`, where the app is bootstrapped. 
For instance, the following piece of code boots the application with `$app->librarian->boot()` and then proceeds to register
the custom tag parser:

```php
# web/index.php
# ...

$app->addService('twig', new TwigServiceProvider());
$app->addService('router', new RouterServiceProvider());
$app->addService('content', new ContentServiceProvider());
$app->addService('librarian', new LibrarianServiceProvider());
$app->addService('devto', new DevtoServiceProvider());

$app->librarian->boot();
$app->content->registerTagParser('video', new VideoTagParser());

# ...
```
_Note: The built-in tag parsers are already registered within ContentParser. These are: `video`, `audio`, `twitter`, `youtube` and `github`._


For instance, if you have in your markdown:

```
{% video /videos/test.mp4 %}
```

It will convert to the tag into the following code:

```html
<video controls>
   <source src="/videos/test.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
```
