---
title: Using Docker and Docker Compose as Development Environment
published: true
description: How to create a new librarian Application using Docker and Docker Compose as development environment.
---

If you'd prefer to use a containerized environment to install and develop your Librarian application, you can use the [librarianphp/librarian-docker](https://github.com/librarianphp/librarian-docker) repository as a base for your setup.

For that, you'll only need Docker and Docker Compose installed on your working machine.

## Downloading the Files
You can download the files in [this repository](https://github.com/librarianphp/librarian-docker) and save them in the root folder of your Librarian application.

The following files are required:
- `docker-compose.yml` - Main configuration for your containerized environment
- `Dockerfile` - This Dockerfile builds a custom app image based on PHP 7.4, with Composer and NPM installed
- `docker-compose/nginx/default.conf` - Nginx configuration file for the containerized web server

Once the files are in place, you can get the environment up and running with:

```shell
docker-compose up -d
```

This will run the containers in background.

To execute commands such as `composer install`, run:

```shell
docker-compose exec app composer install
```

Running NPM:

```shell
docker-compose exec app npm install
```

Compiling css assets:

```shell
docker-compose exec app npm run dev
```

Stopping the environment:

```shell
docker-compose stop
```

Re-starting the environment:

```shell
docker-compose start
```

Destroying the environment:

```shell
docker-compose down
```