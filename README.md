# do-cyberpanel-woocommerce
Deploy WooCommerce on DigitalOcean Droplet using CyberPanel (OpenLiteSpeed).
# WooCommerce Hosting on DigitalOcean with CyberPanel

## Overview
This project demonstrates how to deploy a production-ready WooCommerce store 
on a DigitalOcean droplet using CyberPanel (OpenLiteSpeed).

## Architecture
- DigitalOcean Droplet (Ubuntu 22.04, 2vCPU/4GB RAM)
- CyberPanel with OpenLiteSpeed
- MariaDB for WooCommerce
- SSL with Let's Encrypt
- Optional: Cloudflare CDN + WAF

## Steps
1. Create Droplet on DigitalOcean
2. Install CyberPanel
3. Configure SSL, Email, Backups
4. Install WordPress + WooCommerce
5. Optimize performance with cache + Cloudflare

## Benefits
- Low-cost, production-ready eCommerce
- Automated SSL + backup
- Scalable with DigitalOcean

## Security & Backup Configuration

- **SSL/TLS**: Configured via CyberPanel with Let's Encrypt (auto-renew every 90 days).  
- **Cloudflare SSL/TLS & WAF**: End-to-end encryption with Cloudflare Universal SSL + Web Application Firewall rules.  
- **Backups**: 
  - Application-level backups from CyberPanel (daily).  
  - Droplet snapshots from DigitalOcean (weekly + on-demand).  
  - Option for hourly snapshot for critical workloads.  
- **Firewall Rules**: Configured DigitalOcean firewall to restrict access on ports 80/443 to whitelisted IP ranges. SSH restricted to admin IPs only.  
