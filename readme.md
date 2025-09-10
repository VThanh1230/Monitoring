# Monitoring Project

This project provides a monitoring stack using Docker Compose, Prometheus, and Grafana.

## Features
- **Prometheus**: Collects and stores metrics.
- **Grafana**: Visualizes metrics with customizable dashboards.
- **Docker Compose**: Simplifies deployment and management of services.

## Project Structure
```
monitoring/
├── docker-compose.yml         # Docker Compose configuration
├── prometheus.yml             # Prometheus configuration
├── readme.md                  # Project documentation
└── grafana/
    └── provisioning/
        ├── dashboards.yml     # Grafana dashboards provisioning
        ├── datasources.yml    # Grafana datasources provisioning
        └── dashboards/
            └── dashboard.json # Dashboard structure
```

## Getting Started
1. **Clone the repository**
   ```powershell
   git clone <repo-url>
   cd monitoring
   ```
2. **Start the monitoring stack**
   ```powershell
   docker compose up -d
   ```
3. **Access Grafana**
   - Open your browser and go to: [http://localhost:3001]
   - Default credentials: `admin` / `admin`
4. **Setup Grafana**
   - Go to "Data sources" -> "Add new data source" ->"Prometheus" -> "Connection": Use [http://prometheus:9090] -> "Save & test"
   - Go to "Dashboards" -> "New" -> "Import"
   - Find and import dashboards for common applications at [grafana.com/dashboards] or import via dashboard JSON model -> "Load"
   - Select a Prometheus data source -> Import
