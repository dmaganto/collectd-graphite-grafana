# collectd-graphite-grafana


This repository has been created as a test monitoring stack using diferents solutions:

A) Collectd -> Graphite -> Grafana
B) Collectd -> Prometheus -> Grafana

For (A) stack:
```
cd alpine-collectd
docker built . -t alpine-collectd:0.0.1
cd ..
#Edit docker-compose file choosing alpine-collectd
```

For (B) stack:
```
cd centos-collectd
docker built . -t centos-collectd:0.0.1
cd ..
#Edit docker-compose file choosing centos-collectd
```
