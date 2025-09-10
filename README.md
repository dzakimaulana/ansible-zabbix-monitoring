# Ansible Zabbix Monitoring

Automate adding and removing hosts in **Zabbix** using **Ansible**.

---

## ✨ Features

* Add multiple servers, firewalls, or devices at once.
* Apply **ICMP Ping** and **HTTP 200 checks** automatically.
* Easy cleanup with `state=absent`.
* Separate variables per category (e.g., servers, firewalls).

---

## 📦 Requirements

* **Ansible** ≥ 2.17.4
* **community.zabbix** collection ≥ 4.1.1
* Zabbix server with API access

Install collection:

```bash
ansible-galaxy collection install community.zabbix:>=4.1.1
```

---

## 🚀 Usage

### Add or update hosts

```bash
ansible-playbook -i inventory.ini playbooks/site.yml -e category=servers
```

### Delete hosts

```bash
ansible-playbook -i inventory.ini playbooks/site.yml -e category=servers -e state=absent
```

---

## ✅ Benefits

* Saves time when onboarding many hosts.
* Ensures ICMP and HTTP/HTTPS checks are always consistent.
* Useful for SLA reports (uptime based on ICMP/HTTP monitoring).

---

## 📊 Example Result

After running the playbook, hosts are added into Zabbix automatically and can be included in SLA reports.  

![Zabbix SLA Report](result/example-sla-report.jpg)
