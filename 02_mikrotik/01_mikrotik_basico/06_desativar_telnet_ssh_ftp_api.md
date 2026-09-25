---
title: "Desativar - TELNET, SSH, FTP, API"
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

# 6 - Desativar - TELNET, SSH, FTP, API

```
/ip service set telnet disabled=yes
/ip service set ftp disabled=yes
/ip service set www port=8080
/ip service set ssh disabled=yes
/ip service set api disabled=yes
/ip service set api-ssl disabled=yes
```

---

## 🔗 Notas Relacionadas
- [MikroTik: Acesso SSH via Terminal Linux](12_acesso_ssh_mikrotik_via_terminal_linux.md) — Configuração de chave SSH criptográfica.
- [MikroTik: Gerenciamento de Usuários e Senhas](02_alterando_usuario_senha.md) — Hardening de contas administrativas locais.
- [MikroTik: Proteção Básica de Firewall Stateful](../02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) — Regras de bloqueio na chain input.
