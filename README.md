# Docker Murmur
A Dockerfile with Mumble Server (murmur) built from source with gRPC support enabled.

## Usage

### Setup

```
git clone https://github.com/milleruk/mumble-docker && cd mumble-docker
docker-compose up -d
```

### Connect with Mumble
```
server: localhost
port:   64738
```

Direct Link: `mumble://localhost:64738`

### Custom `murmur.ini`
If you wish to use your own `murmur.ini`, mount it as a volume in your `docker-compose` file or `docker` command:

```yaml
volumes:
  - ./murmur.ini:/etc/murmur/murmur.ini
``` 

### gRPC
`gRPC` is enabled by default by connecting to: `127.0.0.1:50051`
