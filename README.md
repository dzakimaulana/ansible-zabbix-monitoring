# Ansible Zabbix Monitoring

Automates host onboarding and monitoring setup in **Zabbix** using **Ansible**.  
This project provides playbooks to add multiple hosts, apply templates, and configure health checks such as **ICMP ping** and **HTTP 200 response**.

---

## ✨ Features
- Bulk add servers, firewalls, or other devices into Zabbix.
- Apply **ICMP Ping** monitoring automatically.
- Configure **HTTP 200 response checks** for web servers.
- Simple teardown with `state=absent` (no manual cleanup).
- Flexible: separate variables per category (servers, firewalls, etc.).

---

## 📦 Requirements
- **Ansible**: 2.17.4 or later  
- **community.zabbix collection**: 3.3.0  
- Zabbix server with API access