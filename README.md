# Hadoop namenode exporter for Prometheus

Original repository: https://github.com/wyukawa/hadoop_exporter

Exports hadoop namenode metrics via HTTP for Prometheus consumption.

## Changes from the original repository

 - Used glide to manage dependencies
 - Dockerized and deployed to DockerHub for easier access

## How to run

```
docker run epilet/hadoop_exporter \
  -namenode.jmx.url http://localhost:50070/jmx
  -web.listen-address :9070
  -web.telemetry-path /metrics
```
