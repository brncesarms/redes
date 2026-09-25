---
title: "IPs rede interna"
date_created: 2024-02-25
author: "Bruno César"
privacy: public
tags:
  - publico
  - redes
  - redes_basico
---

# IPs rede interna

Veja aqui quais são os IPs que devem ser utilizados numa rede internet
```
10.0.0.0/8 (do IP 10.0.0.1 até 10.255.255.255)
172.16.0.0/12 (do IP 172.16.0.1 até 172.31.255.255)
192.168.0.0/16 (do IP 192.168.0.1 até 192.168.255.255)
```

Não utilize nenhuma outra faixa de IPs em sua rede interna que não sejam listados acima. Podem ser utilizados também IPs públicos fornecidos pela operadora ou os pertencentes ao ASN do provedor.

## Memorizando barramento IPs
```
/24 - 256
/25 - 128
/26 - 64
/27 - 32
/28 - 16
```

---

## 🔗 Notas Relacionadas
- [Redes Wi-Fi: Propagação e Frequências](02_redes_wifi.md) — Fundamentos de RF e boas práticas sem fio.
- [MikroTik: IP, DNS, Pool e Servidor DHCP](../02_mikrotik/01_mikrotik_basico/01_ip_dns_pool_dhcp.md) — Configuração prática de sub-redes e entrega de IP.
- [Arquitetura de Rede, Tailscale e VPN](../04_vpn_tailscale/01_arquitetura_tailscale_vpn_mikrotik.md) — Malhas privadas e VPNs para clientes MikroTik.
- [Guia Principal de Redes](../README.md) — Mapa de conteúdo de redes e conectividade.
