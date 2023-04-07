# BIND Container

[![Docker Pulls](https://img.shields.io/docker/pulls/linuxcontainers/bind.svg)](https://hub.docker.com/r/linuxcontainers/bind/)
[![Docker Stars](https://img.shields.io/docker/stars/linuxcontainers/bind.svg)](https://hub.docker.com/r/linuxcontainers/bind/)
[![Docker Build](https://img.shields.io/docker/cloud/automated/linuxcontainers/bind.svg)](https://hub.docker.com/r/linuxcontainers/bind/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/linuxcontainers/bind.svg)](https://hub.docker.com/r/linuxcontainers/bind/)

[BIND](http://bind9.net/) server running on [Alpine Linux](https://hub.docker.com/_/alpine/).

## Configuration

See [example directory](https://github.com/linuxcontainers/bind/tree/master/example) for sample config file.

## Quickstart

```yml
bind:
  image: linuxcontainers/bind

  volumes:
    # You must provide a config file
    - ./named.conf:/etc/bind/named.conf

    # Zone files
    - ./zones:/var/lib/bind

  ports:
    - "53:53/tcp"
    - "53:53/udp"
```

Excellent work by (https://github.com/jcbiellikltd/docker-bind) for his work
