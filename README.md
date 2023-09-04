# docker-cadvisor

Ready-to-run Docker image with cAdvisor.

## Quickstart

```bash
$ docker run --name cadvisor -e alxshelepenok/cadvisor:latest
```

## Building

```bash
$ ./build.sh latest
```

## Usage

```yaml
version: "3.9"

services:
 cadvisor:
  image: alxshelepenok/cadvisor:latest
  volumes:
    - /:/rootfs:ro
    - /sys:/sys:ro
    - /var/run:/var/run:ro
    - /dev/disk/:/dev/disk:ro
    - /var/lib/docker/:/var/lib/docker:ro
```
