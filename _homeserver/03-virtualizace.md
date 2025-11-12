---
title: Virtualizace (KVM) a Cockpit
order: 3
layout: single
---

Instalace KVM a Cockpit; HAOS běží jako VM kvůli izolaci.

```bash
sudo apt install -y qemu-kvm libvirt-daemon-system libvirt-clients virt-manager cockpit
sudo systemctl enable --now cockpit.socket
```

### Síťový bridge v Netplan (br0)
```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    eno1: { dhcp4: no }
  bridges:
    br0:
      interfaces: [eno1]
      addresses: [192.168.1.250/24]
      gateway4: 192.168.1.1
      nameservers:
        addresses: [192.168.1.251,1.1.1.1]
```
