📦 WordPress + Monitoring Stack with Docker Compose
🔧 Description
This project sets up a complete WordPress development and monitoring environment using Docker Compose. It includes:

WordPress – CMS platform

MySQL – WordPress database

phpMyAdmin – DB management GUI

NGINX – Reverse proxy for WordPress

Grafana – Visualization dashboard

Prometheus – Metrics collection

Node Exporter – Host system metrics

cAdvisor – Container resource monitoring

🚀 Features
📝 WordPress served via NGINX on port 8081

📊 Grafana with Prometheus, Node Exporter, and cAdvisor

🔐 Custom credentials (surya / surya)

🐘 MySQL + phpMyAdmin on port 8083

📡 Live system and container metrics

🛠️ Technologies
Docker & Docker Compose

WordPress + MySQL

Grafana + Prometheus

cAdvisor + Node Exporter

NGINX

phpMyAdmin

📁 Project Structure
bash
Copy
Edit
.
├── docker-compose.yml       # Main Docker Compose file
├── nginx.conf               # NGINX configuration file
└── monitoring/
    └── prometheus.yml       # Prometheus scrape config
⚙️ Getting Started
🧱 Prerequisites
Docker

Docker Compose

Git

▶️ Run the Stack
bash
Copy
Edit
git clone https://github.com/SURYAl3152/Wordpress_Docker_Setup.git
cd Wordpress_Docker_Setup
docker compose up -d --build
🔐 Default Credentials
Service	URL	Username	Password
WordPress	http://localhost:8081	(set on first login)	—
phpMyAdmin	http://localhost:8083	surya	surya
Grafana	http://localhost:3000	surya	surya
Prometheus	http://localhost:9090	—	—
cAdvisor	http://localhost:8085	—	—
Node Exporter	http://localhost:9100/metrics	—	—

Replace localhost with your VM IP (e.g., 192.168.1.6) for access from the host.

📊 Monitoring Sources in Grafana
Prometheus: Data source for all metrics

Node Exporter: Tracks host system resources

cAdvisor: Tracks Docker container metrics

🔁 Reset Grafana Password (if login fails)
bash
Copy
Edit
docker exec -it grafana grafana-cli admin reset-admin-password surya
🧼 Tear Down
bash
Copy
Edit
docker compose down -v
🤝 Author
Surya Loganathan
🌐 LinkedIn
📧 suryaloganathan3152@gmail.com
