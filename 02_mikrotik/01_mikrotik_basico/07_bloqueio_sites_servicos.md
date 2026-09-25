---
title: "Bloqueio: SITES e SERVIÇOS"
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

# 7 - Bloqueio: SITES e SERVIÇOS

```
/ip firewall address-list add address=192.168.10.30 list="Fora do bloqueio do Youtube"
```
 
```
/ip firewall filter add action=drop chain=forward comment="Bloqueio Youtube" content=youtube src-address=192.168.10.0/27 src-address-list="!Fora do bloqueio do Youtube"
```

---

## 🔗 Notas Relacionadas
- [MikroTik: Priorização de Tráfego e QoS](08_priorizar_sites_e_servicos.md) — Marcação e engenharia de tráfego.
- [MikroTik: Servidor DNS Cache](10_servidor_dns_mikrotik.md) — Filtragem estática por resolução DNS.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Proteção de borda e stateful inspection.
