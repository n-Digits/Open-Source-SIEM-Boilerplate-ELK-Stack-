# 🧠 ELK + Filebeat (Open Source SIEM Boilerplate)

A ready-to-deploy **Security Information and Event Management (SIEM)** boilerplate built entirely on **open-source Elastic Stack** components — **Elasticsearch**, **Logstash**, **Kibana**, and **Filebeat** — running via Docker Compose.

This setup allows you to ingest, process, and visualize security logs locally or across your infrastructure. Ideal for testing, SOC labs, or lightweight monitoring setups.

---

## 🚀 Features

✅ Fully Open Source (no license restrictions)  
✅ Preconfigured **Filebeat → Logstash → Elasticsearch → Kibana** pipeline  
✅ Simple one-command startup using Docker Compose  
✅ No x-pack or authentication requirements  
✅ Easily extensible for production environments  
✅ Supports JSON logs, system logs, and container logs  
✅ Kibana-ready for log visualization and analysis  

---

## 🏗️ Stack Overview

The stack consists of four main services:

| Service         | Description |
|-----------------|-------------|
| **Elasticsearch** | Stores indexed logs and event data |
| **Logstash**      | Receives, parses, and forwards logs to Elasticsearch |
| **Kibana**        | Visualizes logs, dashboards, and charts |
| **Filebeat**      | Collects host and container logs and sends them to Logstash |
---

## 📁 Folder Structure
```
elk/
│
├── docker-compose.yml
├── .gitignore
├── README.md
│
├── elasticsearch/
│   └── Dockerfile
│
├── logstash/
│   ├── Dockerfile
│   ├── logstash.conf
│   └── config/
│       └── logstash.yml
│
├── kibana/
│   └── Dockerfile
│
└── filebeat/
    ├── Dockerfile
    └── filebeat.yml
```

## ▶️ Starting the Stack with Docker

1. **Navigate to your project directory**:

```bash
docker-compose up -d --build
```
## 2️⃣ Verify Containers

Run the following command to check that all services are running:

```bash
docker ps
```
**Expected output:**
elasticsearch   Up (healthy)
logstash        Up
kibana          Up
filebeat        Up


## 3️⃣ Open Kibana

Open your browser and navigate to: http://localhost:5601

In Kibana:

Navigate to Stack Management → Index Patterns

Create an index pattern: logs-*

Go to Discover to explore live logs

## 🧠 Extending the SIEM

You can enhance this SIEM setup by:

- Adding [**Metricbeat**](https://www.elastic.co/guide/en/beats/metricbeat/current/metricbeat-overview.html) for system and container metrics
- Adding [**Winlogbeat**](https://www.elastic.co/guide/en/beats/winlogbeat/current/winlogbeat-overview.html) for Windows Event Logs
- Installing [**ElastAlert2**](https://elastalert2.readthedocs.io/en/latest/) for rule-based alerting
- Importing prebuilt [**Kibana dashboards**](https://www.elastic.co/guide/en/kibana/current/saved-objects.html) for visualization
- Forwarding [**Syslog, firewall, or cloud logs**](https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-overview.html) via Filebeat

## ⚠️ Security Notice

This stack disables SSL and authentication for simplicity.  
It is intended for **local testing or lab environments only**.

For production:

- Enable security (`xpack.security.enabled=true`)
- Configure SSL certificates
- Use secure credentials for Elasticsearch and Kibana
- Mount persistent volumes with backups


## 👨‍💻 Maintainer

**n-Digits — AI & Digital Innovation Consulting**  
Perth, Australia  
🌐 [https://n-digits.com](https://n-digits.com)
