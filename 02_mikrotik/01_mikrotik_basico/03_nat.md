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