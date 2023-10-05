# Spring Hello Project

## Project Overview
This is a sample Spring project build with:
- Spring Boot 3
- Maven
- Java 21

## Projects

### Spring Boot (API)
- localhost
- Port: 8080
- Push metrics data to: http://localhost:4318/v1/metrics

### Otel-Collector
- otel-collector
- Port: 8889 (for prometheus)
- Port: 4318:4318
- OTLP http listen at: http://0.0.0.0:4318/v1/metrics

### Prometheus
- prometheus
- Port: 9090
- Scrape data from the Otel Collector endpoint: http://otel-collector:8889

### Grafana (Visualization )
- grafana
- Port: 3000
- Datasource from: http://prometheus:9090

## Endpoints
- **Spring Actuator**: http://localhost:8080/actuator
- **Prometheus**: http://localhost:9090
- **Grafana**: http://localhost:3000