# Tor Docker Proxy
Tor proxy in an Alpine Linux container

## Build

```bash
docker build -t thumbscrew/tor-docker-proxy .
```

## Run with Docker

```bash
docker run --name tor-docker-proxy -p9050:9050 thumbscrew/tor-docker-proxy
```

## Test

```bash
$ curl --socks5 127.0.0.1:9050 https://check.torproject.org/api/ip
{"IsTor":true,"IP":"185.x.x.x"}
```
