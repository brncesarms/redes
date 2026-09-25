---
title: "Mikrotik servidor DNS"
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

# 10 - Mikrotik servidor DNS

 
```
/ip firewall filter add action=drop chain=input comment="drop_ataque_dns_udp" dst-port=53 in-interface=pppoe-brunosiqueira protocol=udp
/ip firewall filter add action=drop chain=input comment="drop_ataque_dns_tcp" dst-port=53 in-interface=pppoe-brunosiqueira protocol=tcp
```

```
/ip firewall nat add action=redirect chain=dstnat comment="focar_dns_local_udp" dst-port=53 in-interface=!pppoe-brunosiqueira protocol=udp to-ports=53
/ip firewall nat add action=redirect chain=dstnat comment="focar_dns_local_tcp" dst-port=53 in-interface=!pppoe-brunosiqueira protocol=tcp to-ports=53
```
 
 
## ou 
 
 
```
/ip firewall filter add action=drop chain=input comment=drop_ataque_dns_udp dst-port=53 in-interface=ether1 protocol=udp
/ip firewall filter add action=drop chain=input comment=drop_ataque_dns_tcp dst-port=53 in-interface=ether1 protocol=tcp
```

```
/ip firewall nat add action=redirect chain=dstnat comment=focar_dns_local_udp dst-port=53 in-interface=!ether1 protocol=udp to-ports=53
/ip firewall nat add action=redirect chain=dstnat comment=focar_dns_local_tcp dst-port=53 in-interface=!ether1 protocol=tcp to-ports=53
```

---

## 🔗 Notas Relacionadas
- [MikroTik: IP, DNS, Pool e Servidor DHCP](01_ip_dns_pool_dhcp.md) — Distribuição automática de DNS para clientes.
- [MikroTik: Bloqueio de Sites e Serviços](07_bloqueio_sites_servicos.md) — Interceptação e redirecionamento de consultas.
- [Guia Principal de Redes](../../README.md) — Mapa de conteúdo de redes.
