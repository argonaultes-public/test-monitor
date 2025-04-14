# Client

```
pip install prometheus-client

```


# Server

## Prometheus

```
docker run prometheus server
```



```bash
docker run \
    -p 9090:9090 \
    -v ./prometheus.yml:/etc/prometheus/prometheus.yml \
    prom/prometheus
```

## VictoriaMetrics

```bash
docker run -it --rm -v ./prometheus.yml:/tmp/config/scrape.yml -p 8428:8428 victoriametrics/victoria-metrics -promscrape.config=/tmp/config/scrape.yml
```