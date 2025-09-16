DigitalOcean WooCommerce Deployment with CyberPanel, Cloudflare & Firewall Hardening

# Project Overview

This project demonstrates a secure and production-ready WooCommerce hosting environment on DigitalOcean Droplet using CyberPanel (OpenLiteSpeed) and Cloudflare.

It covers:

WordPress & WooCommerce deployment on CyberPanel droplet

SSL integration with Let’s Encrypt + Cloudflare Universal SSL

Backup strategy (CyberPanel, DigitalOcean snapshots)

Advanced firewall hardening (restrictive inbound/outbound rules)

# Architecture

Platform: DigitalOcean Droplet (Ubuntu)

Web Server: CyberPanel (OpenLiteSpeed)

Database: MariaDB (auto-installed by CyberPanel)

SSL: Let’s Encrypt (90 days) + Cloudflare SSL

Firewall: DigitalOcean Cloud Firewall

Backups: CyberPanel full site backups + DO hourly snapshots

# Firewall Configuration

Inbound Rules

SSH (22/tcp) – Restricted (Admin IP only)

HTTP (80/tcp) – Allowed only from trusted IPs (DigitalOcean + Cloudflare ranges)

HTTPS (443/tcp) – Allowed only from trusted IPs (DigitalOcean + Cloudflare ranges)

CyberPanel Management (7080/8090) – Restricted to specific IP ranges

Outbound Rules

ICMP – Allowed (All IPv4/IPv6)

All TCP – Allowed (necessary for updates & package downloads)


# Security Hardening

Enforced end-to-end encryption (Let’s Encrypt + Cloudflare SSL).

Disabled public SSH, enabled IP-restricted access only.

Blocked all unused ports by default.

Restricted CyberPanel ports (7080/8090) to known IPs only.

# Backup Strategy

Application Backup – CyberPanel scheduled backups (daily/weekly).

Infrastructure Backup – DigitalOcean droplet snapshots (hourly/daily).

Cloudflare Caching – Protects against downtime and improves performance.
