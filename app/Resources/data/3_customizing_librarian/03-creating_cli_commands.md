---
title: Creating CLI commands
published: true
description: How to create custom CLI commands
---

Librarian is built on top of [Minicli](https://docs.minicli.dev), a minimalist command-line framework in PHP.

You can create custom command-line commands to manage your application, import data, or perform regular scheduled tasks (schedule is possible via Crontab).

Minicli uses a 2-level command structure, with [Namespaces and Controllers](https://docs.minicli.dev/en/latest/02-command_namespaces/). Web controllers are nothing more than commands under the `Web` namespace. The other commands are only run via CLI, with the included `librarian` executable.

For more information on how to create commands, please refer to the [Minicli documentation on how to create commands](https://docs.minicli.dev/en/latest/02-command_namespaces/#creating-a-command-controller).


