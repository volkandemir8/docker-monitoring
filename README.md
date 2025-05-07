# 📦 WordPress Monitoring Stack with Prometheus & Grafana

This project sets up a full monitoring environment using *Docker Compose, including a **WordPress* site with *MySQL* database, *cAdvisor* for container metrics, *Prometheus* for scraping metrics, *Grafana* for visualization, and a *PostgreSQL exporter* for demonstration purposes.

---

## 🧱 Stack Components

* *WordPress*: The CMS being monitored
* *MySQL*: Database service for WordPress
* *cAdvisor*: Collects container-level metrics (CPU, memory, disk, network)
* *Prometheus*: Metrics collection server
* *Grafana*: Metrics visualization platform
* *PostgreSQL Exporter*: Example exporter for PostgreSQL metrics

---

## 🚀 Getting Started

1. *Clone the repository*:

   ```bash
   git clone https://github.com/volkandemir8/docker-monitoring.git
   cd docker-monitoring
    ```

2. *Start all services*:

   ```bash
   docker-compose up -d
   ```

3. *Verify containers*:

   ```bash
   docker ps
   ```

---

## 🌐 Access Web Interfaces

* *WordPress*: [http://localhost:8082](http://localhost:8082)
* *cAdvisor*: [http://localhost:8081](http://localhost:8081)
* *Prometheus*: [http://localhost:9090](http://localhost:9090)
* *Grafana*: [http://localhost:3000](http://localhost:3000)

---

## 📈 Grafana Dashboards

1. Log in to Grafana (admin/admin).
2. Configure Prometheus as a data source (http://prometheus:9090).
3. Import or build dashboards for *container metrics* and *WordPress database metrics*.

---

## 🔧 Environment Variables

* *WORDPRESS\_DB\_HOST*: db
* *WORDPRESS\_DB\_USER*: wordpress
* *WORDPRESS\_DB\_PASSWORD*: wordpress
* *WORDPRESS\_DB\_NAME*: wordpress
* *DATA\_SOURCE\_NAME* (PostgreSQL exporter): postgresql://wordpress:wordpress_password@postgres-db:5432/wordpress

---

## Notes

- Ensure that the `prometheus.yml` file is correctly configured before starting the containers.
- Modify the environment variables in the `docker-compose.yml` file as needed for your setup.

---

## Stopping the Containers

To stop and remove the containers, run:
```bash
docker-compose down
``` 
