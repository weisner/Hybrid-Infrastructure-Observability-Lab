# Hybrid-Infrastructure-Observability-Lab
Build a small enterprise-style environment with Windows, Linux, containers, authentication, APIs, and monitoring.
---
Here is a **clean learning project stack** that covers everything you listed.

---

## Project: Hybrid Infrastructure Observability Lab

Build a **small enterprise-style environment** with Windows, Linux, containers, authentication, APIs, and monitoring.

---

## Core Architecture

**Virtual Infrastructure**

* 1 Hypervisor (Proxmox / VMware / Hyper-V)

**Virtual Machines**

| VM       | OS             | Purpose                 |
| -------- | -------------- | ----------------------- |
| DC01     | Windows Server | Active Directory + LDAP |
| SRV01    | Windows Server | Application / REST API  |
| LNX01    | Ubuntu Server  | Docker host             |
| MON01    | Ubuntu Server  | Monitoring stack        |
| CLIENT01 | Windows 11     | Domain joined testing   |

---

## Components

### Active Directory / LDAP

* Domain: `lab.local`
* Create:

  * Users
  * Groups
  * Service accounts
* Test:

  * LDAP queries
  * Authentication from Linux
  * API authentication

Tools:

* `ldapsearch`
* `sssd`
* `realmd`

---

### Docker Services (LNX01)

Containers:

* **NGINX**
* **PostgreSQL**
* **Sample REST API**
* **Grafana agent**

Example API options:

* FastAPI
* Node Express
* Flask

Functions:

* Read/write users
* Query AD authentication
* Return JSON data

---

### REST API

Example endpoints:

```
GET /health
GET /users
POST /login
GET /metrics
```

Features:

* LDAP authentication
* Database connection
* Logging
* Metrics endpoint

---

### Monitoring Stack (MON01)

Open source stack:

**Prometheus**

* Metrics collection

**Grafana**

* Dashboards

**Loki**

* Logs

**Node Exporter**

* System metrics

**cAdvisor**

* Docker metrics

Monitor:

* CPU
* Memory
* Containers
* API health
* AD server

---

## Testing Scenarios

### Infrastructure

Test:

* Domain join Linux
* AD authentication
* LDAP queries

---

### API

Test with:

```
curl
Postman
k6
```

Test cases:

* login
* API performance
* failure handling

---

### Monitoring

Create dashboards for:

* Docker containers
* API response times
* VM health
* AD server availability

---

## Stretch Goals (Very Valuable)

Add:

**Automation**

* Ansible for VM configuration

**CI/CD**

* GitHub Actions building Docker images

**Infrastructure as Code**

* Terraform for VM deployment

---

## Final Skills Demonstrated

This single lab shows experience with:

* Virtual infrastructure
* Windows + Linux administration
* Docker containerization
* REST API development
* LDAP / Active Directory integration
* Observability and monitoring
* Infrastructure troubleshooting

These map directly to roles like:

* Systems Engineer
* Infrastructure Engineer
* Observability Engineer
* Platform Engineer

---

If you'd like, I can also show you a **much stronger version of this project that looks like real enterprise infrastructure on a resume** (recruiters love it).
