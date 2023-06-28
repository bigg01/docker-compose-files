# Prom stack

```bash
docker-compose up
``` 
Grafana: [http://localhost:3000](http://localhost:3000)
Prometheus: [localhost:9090](localhost:9090)

``` bash
├── READEME.md
├── docker-compose.yaml
├── grafana
│   ├── config.monitoring
│   └── provisioning
│       ├── dashboards
│       │   ├── Docker_Prometheus_Monitoring-1571332751387.json
│       │   └── dashboard.yml
│       └── datasources
│           └── datasource.yml
└── prometheus
    ├── alert.rules
    └── prometheus.yml
```

##  Add custom job to be scrape

```bash
vi prometheus/prometheus.yml

...

  - job_name: 'myserver'

    # Override the global default and scrape targets from this job every 5 seconds.
    scrape_interval: 15s
    static_configs:
      - targets: ['localhost:9000']
...
```
