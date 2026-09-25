---
title: "Removendo SkyNet"
date_created: 2024-02-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - redes
  - ubiquiti
---

# Removendo SkyNet

PuTTY
```
rm /etc/persistent/rc.poststart rm -rf /etc/persistent/.skynet cfgmtd -w -p /etc/  reboot 
```

---

## 🔗 Notas Relacionadas
- [MikroTik Wireless: Canais Brasil 5 GHz](../02_mikrotik/05_mikrotik_wireless/01_canais_brasil_5ghz.md) — Plano de frequência de rádio.
- [MikroTik: Desativação de Serviços Inseguros](../02_mikrotik/01_mikrotik_basico/06_desativar_telnet_ssh_ftp_api.md) — Prevenção contra invasões em equipamentos de rede.
- [Fundamentos de Redes Wi-Fi](../01_redes_basico/02_redes_wifi.md) — Conceitos de redes sem fio.
