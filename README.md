# Prometheus Busybox Docker Base Images

[![Docker Stars](https://img.shields.io/docker/stars/prom/busybox.svg)][hub]
[![Docker Pulls](https://img.shields.io/docker/pulls/prom/busybox.svg)][hub]
[![Image Size](https://img.shields.io/imagelayers/image-size/prom/busybox/latest.svg)][imagelayers]
[![Image Layers](https://img.shields.io/imagelayers/layers/prom/busybox/latest.svg)][imagelayers]

## Tags

### prom/busybox:latest : uClibc

Based on the official `busybox:uclibc` base image.

The following files are added (taken from Debian) to fix some common issues:

- `/etc/ssl/certs/ca-certificates.crt` : for HTTS support
- `/usr/share/zoneinfo` : for timezones

### prom/busybox:glibc : glibc

Based on the official `busybox:glibc` base image.

The following files are added (taken from Debian) to fix some common issues:

- `/etc/ssl/certs/ca-certificates.crt` : for HTTS support
- `/usr/share/zoneinfo` : for timezones
- `/lib/x86_64-linux-gnu/libpthread.so.0` : common required lib for project binaries that cannot be statically builded.


## Update build dependencies

```
$ git clone https://github.com/prometheus/busybox.git
$ make deps
```

## Build Docker images locally

```
$ git clone https://github.com/prometheus/busybox.git
$ make build
```

## More information

  * All of the core developers are accessible via the [Prometheus Developers Mailinglist](https://groups.google.com/forum/?fromgroups#!forum/prometheus-developers) and the `#prometheus` channel on `irc.freenode.net`.

## Contributing

Refer to [CONTRIBUTING.md](CONTRIBUTING.md)

## License

Apache License 2.0, see [LICENSE](LICENSE).


[hub]: https://hub.docker.com/r/prom/busybox/
[imagelayers]: https://imagelayers.io/?images=prom/busybox:latest