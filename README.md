# 🐳 DockerHomeLab

> **A sleek, self-hosted Docker homelab managed with *doco-cd***

![Docker](https://img.shields.io/badge/Docker-Ready-blue)
![Homelab](https://img.shields.io/badge/Homelab-Self--Hosted-success)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---

## ✨ Overview

**DockerHomeLab** is my personal homelab setup built around Docker, designed to be **simple**, **reproducible**, and **automation‑friendly**. The entire stack is managed using **doco-cd**, making deployments predictable and easy to maintain.

This repo serves as:

* 📦 Source of truth for my Docker services
* 🔁 Continuous deployment target via doco-cd
* 🧪 Playground for experimenting with self-hosted services

---

## 🧱 Architecture

* **Container Runtime:** Docker
* **Deployment Model:** GitOps-style via **doco-cd**
* **Networking:** Internal-first, minimal LAN exposure
* **Secrets:** `.env` protected by sops!

---

## 🖥️ Hardware

### The Seb Homelab

* **Device:** Beelink Mini PC
* **Role:** Primary Docker host and my kubernetes cluster manager
* **Form Factor:** Small, quiet, power-efficient

This setup is intentionally modest—optimized for 24/7 uptime without sounding like a jet engine.

---

## 📁 Repository Structure

```text
.
├── .doco-cd.yaml
├── apps/
│   ├── networking/
│   ├── observability/
│   ├── system/
│   └── tools/
└── README.md
```

> *Structure may evolve as the lab grows.*

---

## 🔐 Security Notes

* Secrets are **never committed**
* Services are **not exposed to the LAN by default**
* Reverse proxy / tunnel configs live outside public configs

---

## 🛠️ Tooling

* Docker & Docker Compose
* doco-cd
* GitHub Actions (optional / future)

---

## 🗺️ Roadmap

* [ ] Service documentation per stack
* [ ] Monitoring & alerting
* [ ] Automated backups

---

## 📜 License

This project is for personal and educational use. Fork freely, break things responsibly.

---

💡 *Built for learning, stability, and a little bit of tinkering.*
