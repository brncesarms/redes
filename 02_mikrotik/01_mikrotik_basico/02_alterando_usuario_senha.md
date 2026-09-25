---
title: "Alterar USUÁRIO e SENHA de acesso ao Mikrotik"
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

# 2 - Alterar USUÁRIO e SENHA de acesso ao Mikrotik

 
## Para adicionar
```
/user add group=full name=bruno password=linuxap
```
   
 
## Para remover
```
/user remove admin
```

---

## 🔗 Notas Relacionadas
- [MikroTik: Desativação de Serviços Inseguros](06_desativar_telnet_ssh_ftp_api.md) — Hardening de portas e serviços do RouterOS.
- [MikroTik: Acesso SSH via Terminal Linux](12_acesso_ssh_mikrotik_via_terminal_linux.md) — Automação com chaves criptográficas SSH.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Regras essenciais de proteção do roteador.
