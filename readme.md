# Docker for Prometheus and Grafana

podman run -d --name prometheus  --network aw-network  -p 9090:9090 -v ./config/prometheus.yml:/etc/prometheus/prometheus.yml -v prometheus_data:/prometheus prom/prometheus:latest

podman run -d --name grafana --network aw-network -p 3000:3000 grafana/grafana:latest


podman run -d --name prometheus -p 9090:9090 -v ./config/prometheus.yml:/etc/prometheus/prometheus.yml -v prometheus_data:/prometheus prom/prometheus:latest

podman run -d --name grafana -p 3000:3000 grafana/grafana:latest
