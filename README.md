This repo contains example configurations for running the Kaazing gateway.  All the configurations are tested using [Docker](https://docs.docker.com/mac/started/) and [Docker Compose](https://docs.docker.com/compose/)

### Getting Started

1. Build dockerized.gateway and dockerized.broker
```bash
cd dockerized.gateway
docker build -t "gateway.ex.base" dockerized.gateway
docker build -t "broker.ex.base" dockerized.broker
```
