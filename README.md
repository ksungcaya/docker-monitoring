## Monitoring
Docker containers monitoring stack.

### Prometheus
Stack uses [cAdvisor](https://github.com/google/cadvisor) and [node_exporter](https://github.com/prometheus/node_exporter) for collection, [Prometheus](https://prometheus.io/) for storage, [Grafana](http://grafana.org/) for visualisation. While Prometheus's [Alertmanager](https://github.com/prometheus/alertmanager) sends notifications to the configured receivers in ```alertmanager/config.yml```.

The default dashboard was exported from [here](https://grafana.com/dashboards/395).

### Influxdb
Stack uses [telegraf](https://www.influxdata.com/time-series-platform/telegraf/) for collection and [InfluxDB](https://www.influxdata.com/time-series-platform/influxdb/) for storage.



## Run using docker-compose
``` bash
docker-compose -f docker-compose.yml -f docker-compose{influxdb|prometheus}.yml up -d
```

## Todo
1. Include logging stack.
2. Improve ```README```.
3. Configure envs.
4. Improve ```prometheus/rules/*```.
5. Grafana dashboard for influxdb source.
