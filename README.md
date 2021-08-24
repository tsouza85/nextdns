# nextdns

This is a nextdns client into a single package

## Example usage

Here is an example docker-compose.yml file that will setup docker services.

```
version: "3"
services:
  nextdns:
    image: tsouza85/nextdns:latest
    container_name: nextdns
    network_mode: "host"
    environment:
      - NEXTDNS_CONFIG=your_nextdns_id
    ports:
      - 53:53/udp
    extra_hosts: #optional
      - "host.local.domain host.local: 192.168.0.10"
    restart: always
```

To use the compose file, just make it in the directory of your choice, then simply run:

`docker-compose up -d`
