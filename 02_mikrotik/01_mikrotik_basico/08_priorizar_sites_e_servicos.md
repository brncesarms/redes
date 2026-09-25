---
title: "Priorizar - SITE e SERVIÇOS"
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

# 8 - Priorizar - SITE e SERVIÇOS

```
/ip firewall mangle 
add action=add-dst-to-address-list address-list=Lista-IPTV address-list-timeout=1d chain=prerouting content=tv5.cs10.tv src-address=192.168.11.0/24 
add action=mark-connection chain=prerouting dst-address-list=Lista-IPTV new-connection-mark=tv-conexoes passthrough=yes 
add action=mark-packet chain=prerouting connection-mark=tv-conexoes new-packet-mark=tv-pacotes passthrough=yes
```

```
/queue tree 
add limit-at=3M max-limit=3M name=IPTV packet-mark=tv-pacotes parent=global priority=1
```

---

## 🔗 Notas Relacionadas
- [MikroTik: Controle de Banda por IP (Simple Queues)](09_controle_de_banda_por_ip.md) — Limitação de taxa de upload/download por host.
- [MikroTik: Bloqueio de Sites e Serviços](07_bloqueio_sites_servicos.md) — Políticas de acesso e listas de controle.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Regras de filtragem e FastTrack.
