# Terraform-Provisioned Monitoring & Alerting Stack  
**Prometheus · Grafana · Alertmanager**

## Overview
This project implements a **production-style monitoring and alerting stack** using **Prometheus, Grafana, and Alertmanager**, with infrastructure provisioned using **Terraform on AWS**. The system collects infrastructure metrics, visualizes them through Grafana dashboards, and sends automated alerts via email when defined thresholds are exceeded.

The goal of this project is to demonstrate **observability practices used in real DevOps environments**, including infrastructure monitoring, alerting pipelines, and secure configuration management.

---

## Architecture
            +------------------+
            |      Users       |
            +---------+--------+
                      |
                      v
                Grafana Dashboards
                      |
                      v
                 Prometheus
           (Metrics Collection)
                      |
                      v
                 Node Exporter
           (Infrastructure Metrics)
                      |
                      v
                 Alert Rules
                      |
                      v
                Alertmanager
                      |
                      v
               Email Notifications




Infrastructure provisioning is handled using **Terraform**, which creates the required AWS resources and prepares the environment for the monitoring stack.

---

## Features

- Infrastructure provisioning using **Terraform**
- Containerized monitoring stack using **Docker Compose**
- Real-time infrastructure monitoring via **Prometheus**
- Custom dashboards using **Grafana**
- Alert routing and notification using **Alertmanager**
- Email notifications through **SMTP**
- Secure credential management using **environment variables**

---

## Tech Stack

- **Terraform** – Infrastructure as Code  
- **AWS EC2** – Compute infrastructure  
- **Docker & Docker Compose** – Containerized services  
- **Prometheus** – Metrics collection and alert rules  
- **Grafana** – Visualization and dashboards  
- **Alertmanager** – Alert routing and notifications  
- **Node Exporter** – System metrics exporter  
- **SMTP (Gmail)** – Email alert notifications  


---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/terraform-monitoring-stack.git
cd terraform-monitoring-stack
```

### 2. Configure Environment Variables

```bash
SMTP_FROM=your_email@gmail.com
SMTP_USERNAME=your_email@gmail.com
SMTP_PASSWORD=your_gmail_app_password
ALERT_RECEIVER_EMAIL=receiver_email@gmail.com
```

### 3. Configure Environment Variables

```bash
cd terraform
terraform init
terraform plan
terraform apply
```

### 4. Start the Monitoring Stack

```bash
docker-compose up -d
```

### 5. Access Services

 #### Prometheus
```bash
http://EC2_PUBLIC_IP:9090
```

 #### Grafana
```bash
http://EC2_PUBLIC_IP:Grafana
```

 #### Alertmanager
```bash
http://EC2_PUBLIC_IP:9093
```

 #### Default Grafana login:
```bash
username: admin
password: admin
```





               
