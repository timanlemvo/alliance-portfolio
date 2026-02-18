# Tima Nlemvo

Senior IT Engineer transitioning into Systems / DevOps / Cloud Engineering.  
7+ years of enterprise IT across identity, endpoints, and infrastructure.  
Based in Los Angeles, CA.

---

## The Alliance Fleet

A production-grade 3-node Proxmox cluster running 25+ services across compute, storage, and security. Built to design, break, diagnose, and document real infrastructure — not follow tutorials.

| Node | Alias | Role |
|------|-------|------|
| Node-A | Millennium Falcon | AI/ML compute, GPU passthrough, LLM inference |
| Node-B | CR90 Corvette | Data operations, identity, observability |
| Node-C | Gozanti Cruiser | Network security, DNS filtering, SIEM |

**Stack:** Proxmox VE · Wazuh · Authentik · InfluxDB · Telegraf · Grafana · Nginx Proxy Manager · AdGuard · n8n · Ollama · PostgreSQL · Vaultwarden · Tailscale

**Architecture:** 4 VLANs (Management, Services, IoT, DMZ) · Zero-trust access · Full observability pipeline · VFIO GPU passthrough

---

## Highlighted Projects

**SIEM Automation Pipeline**  
Wazuh for threat detection + n8n for orchestration + Discord webhooks for alerting. Automated brute-force blocking and file integrity monitoring.

**Zero-Trust Identity Platform**  
Authentik OIDC/SAML across 15+ services. 100% MFA enforcement, full audit logging, no password sprawl.

**GPU AI Platform**  
RTX 4000 Ada via VFIO passthrough. Ollama for local LLM inference at 50 tok/s on 70B models. 500+ document RAG pipeline. Zero data egress.

---

## Writeups

Engineering documentation from real incidents and infrastructure decisions.

**Diagnosing a Silent Hard Lockup on a Proxmox VFIO Passthrough Node**  
Node-A suffered a complete lockup with zero local crash artifacts — no kernel panic, no pstore, no journal entries. Root cause isolated using external Telegraf/InfluxDB telemetry from Node-B. PCIe bus stall from NVIDIA GPU under VFIO passthrough. Fixed with kernel mitigations and log2ram removal.

Full blog: [holocron-labs.tima.dev](https://holocron-labs.tima.dev)  
Writeups repo: [technical-writeups](https://github.com/timanlemvo/technical-writeups)

---

## Background

**Team Liquid** — Senior IT Engineer (2023–Present)  
**Stagwell** — Senior IT Engineer (2021–2023)  
**Creative Artists Agency** — IT Engineer (2019–2021)

Full Stack Web Development — UCLA Extension (2021)

---

## Currently Working On

- Understanding and learning Kubernetes (k3s) on Node-B
- Terraform for VM provisioning
- Proxmox Backup Server with offsite replication
- Azure integration

---

[tima.dev](https://tima.dev) · [linkedin.com/in/timanlemvo](https://linkedin.com/in/timanlemvo) · [TimaNlemvo@gmail.com](mailto:TimaNlemvo@gmail.com)
