# 📊 Monitoring Stack - Zabbix + Prometheus + Grafana

Projeto de monitoramento completo utilizando Docker Compose.

## 🚀 Objetivo

Implementar uma stack de observabilidade em ambiente Linux, simulando cenário real de produção.

## 🏗️ Arquitetura

- Zabbix Server
- Zabbix Agent2
- MySQL 8
- Prometheus
- Grafana
- Docker & Docker Compose
- Ubuntu 24.04

Infra hospedada em Droplet da DigitalOcean.

---

## 📦 Serviços

| Serviço | Porta |
|----------|--------|
| Zabbix Web | 80 |
| Zabbix Server | 10051 |
| Prometheus | 9090 |
| Grafana | 3000 |

---

## ▶️ Como subir o ambiente

```bash
docker-compose up -d
