# Prom stack

`docker-compose -f docker-compose.yaml up`

Grafana: localhost:3000
Prometheus: localhost:9090

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
