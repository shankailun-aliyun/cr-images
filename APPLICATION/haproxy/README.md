# HAProxy 

# Quick reference

- Maintained by: [OpenAnolis CloudNative SIG](https://openanolis.cn/sig/cloud-native)
- Where to get help: [OpenAnolis CloudNative SIG](https://openanolis.cn/sig/cloud-native)

# Supported tags and respective `Dockerfile` links

- [`1.8.27-8.6`, `latest`](https://gitee.com/anolis/docker-images/blob/master/haproxy/1.8.27/8.6/Dockerfile)

# Supported architectures

- arm64, x86-64

# Build reference

## Build multi-arch images and push to registry:
```shell
docker buildx build -t "openanolis/haproxy:$VERSION" --platform linux/amd64,linux/arm64 . --push
```

# Test the configuration file

```shell
docker run -it --rm --name haproxy-syntax-check openanolis/haproxy haproxy -c -f /etc/haproxy/haproxy.cfg
```

# Usage

```shell
docker run -d --name my-running-haproxy openanolis/haproxy
```

# HAProxy
HAProxy is a free, open source high availability solution, providing load balancing and proxying for TCP and HTTP-based applications by spreading requests across multiple servers. It is written in C and has a reputation for being fast and efficient (in terms of processor and memory usage).
