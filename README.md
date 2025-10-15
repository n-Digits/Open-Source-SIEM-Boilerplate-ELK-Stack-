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
cd path/to/elk
```

## 👨‍💻 Maintainer

**n-Digits — AI & Digital Innovation Consulting**  
Perth, Australia  
🌐 [https://n-digits.com](https://n-digits.com)
