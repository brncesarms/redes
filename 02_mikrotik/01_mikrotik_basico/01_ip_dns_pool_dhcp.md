---
title: "IP, DNS, POOL e DHCP"
date_created: 2024-02-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - redes
  - mikrotik
  - mikrotik_basico
  - routeros
---

# 1 - IP, DNS, POOL e DHCP


## IP
```
/ip address add address=192.168.10.1/24 interface=LAN network=192.168.10.0

```
   
## DNS
```
/ip dns set servers=1.0.0.1,8.8.4.4,208.67.220.220

```
   
## POOL
```
/ip pool add name=dhcp_pool0 ranges=192.168.10.2-192.168.10.254

```
 
## DHCP SERVER
```
/ip dhcp-server add address-pool=dhcp_pool0 disabled=no interface=LAN name=dhcp1

```
 
```
/ip dhcp-server network add address=192.168.10.0/24 dns-server=8.8.4.8,1.0.0.1 gateway=192.168.10.1

```

---

## 🔗 Notas Relacionadas
- [MikroTik: Source NAT Masquerade](03_nat.md) — Tradução de endereços para saída à Internet.
- [MikroTik: Servidor DNS Cache](10_servidor_dns_mikrotik.md) — Cache local de nomes e resolução estática.
- [Fundamentos de IPs e Sub-redes](../../01_redes_basico/01_ips_rede_interna.md) — Dimensionamento de pools e faixas de rede privada.
- [Guia Principal de Redes](../../README.md) — Índice completo de engenharia de redes.
