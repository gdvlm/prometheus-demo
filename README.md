# Prometheus Demo
Simple repository to spin up a Prometheus docker instance for demo purposes.

## Containers

The docker compose file includes the following services:
* **prometheus** - scrapes data using the config and allows querying via the dashboard
* **alert manager** - allows for granular control over prometheus alerts
* **cadvisor** - monitors and presents resource usage of running containers
* **redis** - example service to collect data from
* **grafana** - ingests metrics from prometheus and allows for powerful visualization capabilities
  * Prometheus will be need to be added as a data source using [this guide](https://prometheus.io/docs/tutorials/visualizing_metrics_using_grafana/)

## Run

Run in the root directory to spin up services in detached mode:
```
docker compose up -d
```

## Links

Open the following links to view the services:
* Prometheus:    http://localhost:9090
* Alert Manager: http://localhost:9093
* cAdvistor:     http://localhost:8080
* Grafana:       http://localhost:3000

Connect to Redis using a database IDE at: http://localhost:6379/

## Screenshots

Prometheus:

<img width="1302" alt="prometheus" src="https://github.com/user-attachments/assets/f79950df-6fa4-4eb0-ba72-f8a9345c1316" />


cAdvisor:

<img width="1169" alt="cadvisor" src="https://github.com/user-attachments/assets/eb890478-c5bb-4723-8551-f9d565161f20" />


Grafana:

<img width="1303" alt="grafana" src="https://github.com/user-attachments/assets/bd6753f4-e2dd-420b-9292-642107ab075e" />
