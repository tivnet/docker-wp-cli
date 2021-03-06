# WP-CLI

[![Build Status][travis-image]][travis-url]
[![Docker Automated build][docker-image]][docker-url]
[![Docker Repository on Quay][quay-image]][quay-url]
[![Metadata][micro-badger-image]][micro-badger-url]

[Alpine Linux][alpine-linux] based Docker image for [WP-CLI][wp-cli].

> WP-CLI is a set of command-line tools for managing WordPress installations.

## Installation

Pull the image from Docker Hub.

```sh
docker pull devaloka/wp-cli
```

Or, pull the image from Quay.

```sh
docker pull quay.io/devaloka/wp-cli
```

## Usage

### Run the image pulled from Docker Hub

Mount a data-volume-container and run WP-CLI.

```sh
docker run --rm -it -u <uid>:<gid> -v <data-volume-container> devaloka/wp-cli <command>
```

Mount a host directory and run WP-CLI.

```sh
docker run --rm -it -u "$UID:$(id -g)" -v "$(pwd)/wp:/wp-cli" devaloka/wp-cli <command>
```

### Run the image pulled from Quay

Mount a data-volume-container and run WP-CLI.

```sh
docker run --rm -it -u <uid>:<gid> -v <data-volume-container> quay.io/devaloka/wp-cli <command>
```

Mount a host directory and run WP-CLI.

```sh
docker run --rm -it -u "$UID:$(id -g)" -v "$(pwd)/wp:/wp-cli" quay.io/devaloka/wp-cli <command>
```

[alpine-linux]: https://alpinelinux.org
[wp-cli]: http://wp-cli.org

[travis-image]: https://travis-ci.org/devaloka/docker-wp-cli.svg?branch=master
[travis-url]: https://travis-ci.org/devaloka/docker-wp-cli

[docker-image]: https://img.shields.io/docker/automated/devaloka/wp-cli.svg
[docker-url]: https://hub.docker.com/r/devaloka/wp-cli/

[micro-badger-image]: https://images.microbadger.com/badges/image/devaloka/wp-cli.svg
[micro-badger-url]: https://microbadger.com/images/devaloka/wp-cli

[quay-image]: https://quay.io/repository/devaloka/wp-cli/status
[quay-url]: https://quay.io/repository/devaloka/wp-cli
