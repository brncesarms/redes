---
title: "Automatic reboot mikrotik"
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

# Automatic reboot mikrotik

## Script
```bash
system script

```

```bash
add dont-require-permissions=no name=automatic_reboot owner=suporte policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon source=\
    "system reboot\r\
    \ny\r\
    \n"

```

## Scheduler
```bash
system scheduler

```

```bash
add interval=1d name=schedule_automatic_reboot on-event=\
    schedule_automatic_reboot policy=\
    ftp,reboot,read,write,policy,test,password,sniff,sensitive,romon \
    start-date=feb/25/2024 start-time=04:00:00

```

---

## 🔗 Notas Relacionadas
- [MikroTik: IP, DNS, Pool e Servidor DHCP](01_ip_dns_pool_dhcp.md) — Serviços essenciais do roteador.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Segurança de borda contínua.
- [Guia Principal de Redes](../../README.md) — Índice principal.
