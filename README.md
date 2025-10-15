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

## 🏗️ Architecture Overview
[Filebeat] → [Logstash] → [Elasticsearch] → [Kibana]

| Component        | Port  | Description |
|------------------|-------|-------------|
| **Elasticsearch** | 9200 | Stores and indexes logs |
| **Logstash**      | 5000 / 5044 / 9600 | Receives, filters, and forwards logs |
| **Kibana**        | 5601 | Web interface for dashboards and searches |
| **Filebeat**      | — | Collects logs from containers or host |

---

## 📁 Folder Structure
elk/
│
├── docker-compose.yml
├── .gitignore
├── README.md
│
├── elasticsearch/
│ └── Dockerfile
│
├── logstash/
│ ├── Dockerfile
│ ├── logstash.conf
│ └── config/
│ └── logstash.yml
│
├── kibana/
│ └── Dockerfile
│
└── filebeat/
├── Dockerfile
└── filebeat.yml

## ▶️ Running the Stack

docker-compose up -d --build

