---
title: "Exemplo_sumarização_OSPF"
date_created: 2024-02-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - redes
  - mikrotik
  - mikrotik_roteamento
  - routeros
---

# Exemplo_sumarização_OSPF

```
/routing ospf area 
add area-id=0.0.0.1 name=PPPoE_Clientes
```

```
/routing ospf area range 
add area=PPPoE_Clientes range=10.250.2.0/24
```

```
/routing ospf network 
add area=PPPoE_Clientes comment=PPPoE_Clientes network=10.250.2.0/24
```

---

## 🔗 Notas Relacionadas
- [MikroTik no EVE-NG](../03_mikrotik_eve_ng/01_eve_ng.md) — Ambiente de simulação para validação de roteamento dinâmico.
- [Fundamentos de IPs e Sub-redes](../../01_redes_basico/01_ips_rede_interna.md) — Cálculo de blocos CIDR para sumarização.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Regras para tráfego entre áreas OSPF.
