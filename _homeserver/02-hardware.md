---
title: Hardware a instalace OS
order: 2
layout: single
---

MSI Cubi 5 12M, i7, 32 GB RAM, NVMe + SATA. Instalace **Ubuntu Server LTS** v režimu UEFI.

### Základní nastavení po instalaci
```bash
sudo apt update && sudo apt -y upgrade
sudo timedatectl set-timezone Europe/Prague
sudo adduser deploy && sudo usermod -aG sudo,adm,plugdev,docker deploy || true
```
