---
title: "NAT"
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

# 3 - NAT

```
/ip firewall nat add action=masquerade chain=srcnat comment=Full-masquerade
```
 
## ou

```
/ip firewall nat add action=masquerade chain=srcnat comment=Mascaramento out-interface=ether1
```

---

## 🔗 Notas Relacionadas
- [MikroTik: Zona Desmilitarizada (DMZ)](04_dmz.md) — Isolamento e encaminhamento para hosts públicos.
- [MikroTik: Redirecionamento de Portas (Dst-NAT)](05_redirecionamento_porta.md) — Encaminhamento seletivo de serviços internos.
- [MikroTik: IP, DNS, Pool e Servidor DHCP](01_ip_dns_pool_dhcp.md) — Entrega de IPs e gateway aos clientes locais.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Regras de filtragem e FastTrack no firewall.
