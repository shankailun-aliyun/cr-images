# Grafana

# Quick reference

- Maintained by: [OpenAnolis CloudNative SIG](https://openanolis.cn/sig/cloud-native)
- Where to get help: [OpenAnolis CloudNative SIG](https://openanolis.cn/sig/cloud-native)

# Supported tags and respective `Dockerfile` links

- [`7.5.11-8.6`, `latest`](https://gitee.com/anolis/docker-images/blob/master/grafana/7.5.11/8.6/Dockerfile)

# Supported architectures

- arm64, x86-64

# Build reference

## Build multi-arch images and push to registry:
```shell
docker buildx build -t "openanolis/grafana:$VERSION" --platform linux/amd64,linux/arm64 . --push
```

# Usage
```shell
docker run -d --name=grafana -p 3000:3000 openanolis/grafana
```

# Grafana
The open-source platform for monitoring and observability. Grafana allows you to query, visualize, alert on and understand your metrics no matter where they are stored. Create, explore, and share dashboards with your team and foster a data-driven culture.
