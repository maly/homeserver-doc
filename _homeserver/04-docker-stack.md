---
title: Docker stack a struktura
order: 4
layout: single
---

Samostatné stacky v `~/docker/**`. Portainer pro správu, Watchtower pro aktualizace (nebo manuální skripty).

### Ukázka `docker-compose.yml` (výřez)
```yaml
services:
  portainer:
    image: portainer/portainer-ce:latest
    ports: ["9443:9443"]
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
      - portainer_data:/data
  adguardhome:
    image: adguard/adguardhome:latest
    network_mode: host
    volumes:
      - ./adguard/work:/opt/adguardhome/work
      - ./adguard/conf:/opt/adguardhome/conf
```
