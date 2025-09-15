# grafana-prometheus-stack

# Docker Monitoring Stack 🚀

A complete observability setup using Docker Compose with:

- **Prometheus** for metrics collection
- **Grafana** for visualization
- **Loki** and **Promtail** for logs
- **Node Exporter** for host metrics
- **NGINX Exporter** for NGINX metrics

---

## 🧱 Stack Components

| Component        | Port  | Description                              |
|------------------|-------|------------------------------------------|
| Grafana          | 3000  | Dashboards and visualizations            |
| Prometheus       | 9090  | Metrics scraping and querying            |
| Loki             | 3100  | Log aggregation                          |
| Promtail         | 9080* | Log collector (internal only)            |
| Node Exporter    | 9100* | Host metrics (internal only)             |
| NGINX Exporter   | 9113* | NGINX metrics (internal only)            |

---

## 🚀 Getting Started

### 1. Clone the Repository
git clone https://github.com/yourusername/docker-monitoring-stack.git
cd docker-monitoring-stack

### 2. Setup Configuration Files
Ensure the following files exist in the root directory:
* prometheus.yml
* promtail-config.yml
* loki-config.yml
Customize them as needed for your setup.

### 3. Run the Stack
docker-compose up -d

### 4. Access the Tools
Grafana: http://localhost:3000
Default credentials: admin / admin
Prometheus: http://localhost:9090
Loki: http://localhost:3100

### 📊 Dashboards & Alerts
Import official dashboards from Grafana.com for:
* Prometheus Node Exporter
* Loki logs
* NGINX metrics
You can also create alerts in Grafana using Prometheus metrics or log queries from Loki.

### 🛠️ Requirements
* Docker
* Docker Compose
* NGINX with stub_status enabled (for metrics)
* SMTP credentials (optional, for email alerts)
