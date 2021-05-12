---
title: Creating CLI commands
published: true
description: How to create custom CLI commands
---

Librarian is built on top of [Minicli](https://docs.minicli.dev), a minimalist command-line framework in PHP.

You can create custom command-line commands to manage your application, import data, or perform regular scheduled tasks (schedule is possible via Crontab). These should be created within the `app/Command` directory.

The included `librarian` executable loads a few example commands that you can use as reference to build your own.

### About Minicli
Minicli uses a 2-level command structure, with [Namespaces and Controllers](https://docs.minicli.dev/en/latest/02-command_namespaces/). Web controllers are nothing more than commands under the `Web` namespace. The other commands are only run via CLI, with the included `librarian` executable.

### Default Command Structure

This is how the default command structure looks like by default in a fresh Librarian install:

```shell
app/Command
├── Cache
│   ├── ClearController.php
│   └── RefreshController.php
├── Create
│   └── ContentController.php
├── Help
│   ├── DefaultController.php
│   └── TestController.php
├── Import
│   └── DevToController.php
└── Web
    ├── ContentController.php
    ├── ErrorController.php
    ├── FeedController.php
    ├── IndexController.php
    ├── NotFoundController.php
    └── TagController.php

```

This yields the following command tree:

![Librarian help CLI](/img/librarian_help.png)

For more information on how to create commands, please refer to the [Minicli documentation on how to create commands](https://docs.minicli.dev/en/latest/02-command_namespaces/#creating-a-command-controller).


