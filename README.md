This repo contains example configurations for running the Kaazing gateway.  All the configurations are tested using [Docker](https://docs.docker.com/mac/started/) and [Docker Compose](https://docs.docker.com/compose/)

### Setup

All setups assume you have an /etc/host entry for gateway.example.com pointing to your docker host ip.
The docker host ip can be found via `docker-machine ip dockermachine`

example /etc/hosts entry
```
192.168.99.100 gateway.example.com 
```

### Launching Echo Service

```bash
docker build -t dockerized.gateway dockerized.gateway
docker run --name=gateway -h gateway.example.com dockerized.gateway
docker kill gateway
```

### Launching JMS WebSocket Service 

```bash
docker-compose -f jms.and.broker.yml up
docker-compose -f jms.and.broker.yml rm
```

### Launching KWIC demo
```bash
docker-compose -f kwic.yml up
```

To Test run `nc gateway.example.com 9000`
