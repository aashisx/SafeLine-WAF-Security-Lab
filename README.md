# SafeLine WAF Security Lab

A practical cybersecurity laboratory demonstrating the deployment and testing of **SafeLine Web Application Firewall (WAF)** in front of a deliberately vulnerable web application, DVWA.

The project focuses on HTTPS reverse proxying, WAF protection, SQL injection detection, HTTP flood protection, and source-IP access control in an isolated virtualized environment.

---

## 📌 Project Overview

Web applications can be exposed to various application-layer attacks such as SQL injection, excessive request traffic, and unauthorized access.

This project demonstrates how a Web Application Firewall can be placed between a security testing machine and a vulnerable web application to inspect and control incoming requests.

The laboratory uses:

- **SafeLine WAF** as the security and reverse-proxy layer
- **DVWA** as the intentionally vulnerable web application
- **Apache** as the web server
- **Ubuntu Server** as the server environment
- **Kali Linux** as the security testing machine
- **HTTPS/TLS** for encrypted communication

---

## 🏗️ Lab Architecture

```text
                    HTTPS :443
                 https://dvwa.local
                        │
                        ▼
              ┌───────────────────┐
              │    SafeLine WAF   │
              │  Reverse Proxy    │
              │  Security Layer   │
              └─────────┬─────────┘
                        │
                        │ HTTP :8080
                        ▼
              ┌───────────────────┐
              │   Apache + DVWA   │
              │   Ubuntu Server   │
              └───────────────────┘
                        ▲
                        │
                  Security Testing
                        │
                  ┌─────┴─────┐
                  │ Kali Linux│
                  └───────────┘