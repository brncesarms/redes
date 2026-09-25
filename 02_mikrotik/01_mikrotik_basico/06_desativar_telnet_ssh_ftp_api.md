---
title: "Desativar - TELNET, SSH, FTP, API"
date_created: 2024-02-25
author: "Bruno César / Antigravity"
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