---
title: "Removendo SkyNet"
date_created: 2024-02-25
author: "Bruno César / Antigravity"
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

