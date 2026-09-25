---
title: "Exemplo_sumarização_OSPF"
date_created: 2024-02-25
author: "Bruno César / Antigravity"
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