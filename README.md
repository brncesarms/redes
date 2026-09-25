---
title: "Redes e Conectividade — Mapa de Conteúdo"
date_created: 2024-02-25
date_updated: 2026-09-19
tags:
  - redes
  - mikrotik
  - ubiquiti
  - moc
  - indice
---

# 🔌 Redes e Conectividade — Mapa de Conteúdo

Guias práticos de configuração, administração e segurança para equipamentos de rede, roteamento RouterOS (MikroTik), wireless e switches.

## 📂 Sub-Áreas

| # | Sub-Área | Notas | Foco Principal |
|---|----------|-------|----------------|
| 🌐 | [`01_redes_basico`](./01_redes_basico/) | 2 notas | Endereçamento IP interno, classes e redes Wi-Fi |
| 🛡️ | [`02_mikrotik`](./02_mikrotik/) | 19 notas | RouterOS, DHCP, Firewall, NAT, OSPF, EVE-NG, Wireless |
| 📡 | [`03_ubiquiti`](./03_ubiquiti/) | 1 nota | Manutenção e procedimentos em equipamentos Ubiquiti |

---

## 📑 Índice Detalhado de Notas

### 🌐 1. Fundamentos de Redes
- [IPs de Rede Interna](./01_redes_basico/01_ips_rede_interna.md)
- [Redes Wi-Fi](./01_redes_basico/02_redes_wifi.md)

### 🛡️ 2. MikroTik (RouterOS)
- **Configuração Básica:**
  - [IP, DNS, Pool e DHCP Server](./02_mikrotik/01_mikrotik_basico/01_ip_dns_pool_dhcp.md)
  - [Alterando Usuário e Senha](./02_mikrotik/01_mikrotik_basico/02_alterando_usuário_senha.md)
  - [Configuração de NAT](./02_mikrotik/01_mikrotik_basico/03_nat.md)
  - [DMZ (Zona Desmilitarizada)](./02_mikrotik/01_mikrotik_basico/04_dmz.md)
  - [Redirecionamento de Portas](./02_mikrotik/01_mikrotik_basico/05_redirecionamento_porta.md)
  - [Desativar Telnet, SSH, FTP e API](./02_mikrotik/01_mikrotik_basico/06_desativar_telnet_ssh_ftp_api.md)
  - [Bloqueio de Sites e Serviços](./02_mikrotik/01_mikrotik_basico/07_bloqueio_sites_serviços.md)
  - [Priorização de Tráfego e Serviços](./02_mikrotik/01_mikrotik_basico/08_priorizar_sites_e_serviços.md)
  - [Controle de Banda (Queue por IP)](./02_mikrotik/01_mikrotik_basico/09_controle_de_banda_por_ip.md)
  - [Servidor DNS Cache no MikroTik](./02_mikrotik/01_mikrotik_basico/10_servidor_dns_mikrotik.md)
  - [Habilitar RoMON](./02_mikrotik/01_mikrotik_basico/11_habilitar_romon.md)
  - [Acesso SSH ao MikroTik via Terminal Linux](./02_mikrotik/01_mikrotik_basico/12_acesso_ssh_mikrotik_via_terminal_linux.md)
  - [Script de Provisionamento SXT](./02_mikrotik/01_mikrotik_basico/script_sxt_2016.md)
  - [Reboot Automático Programado](./02_mikrotik/automatic_reboot.md)
- **Segurança & Firewall:**
  - [Regras Básicas de Proteção de Firewall](./02_mikrotik/02_mikrotik_firewall/01_básico_para_proteger_seu_mikrotik.md)
- **Roteamento Avançado:**
  - [Sumarização de Rotas no OSPF](./02_mikrotik/04_mikrotik_roteamento/01_exemplo_sumarização_ospf.md)
- **Laboratórios & Virtualização:**
  - [MikroTik no EVE-NG](./02_mikrotik/03_mikrotik_eve_ng/01_eve_ng.md)
- **Wireless & Enlaces:**
  - [Canais Regulamentados Brasil 5 GHz](./02_mikrotik/05_mikrotik_wireless/01_canais_brasil_5ghz.md)
  - [Análise Espectral (Spectral Scan)](./02_mikrotik/05_mikrotik_wireless/02_analise_espectral.md)

### 📡 3. Ubiquiti
- [Removendo Skynet de Equipamentos Ubiquiti](./03_ubiquiti/01_removendo_skynet.md)

---

## 🔗 Referências
- Documentação Oficial: [MikroTik Wiki & RouterOS Docs](https://wiki.mikrotik.com/wiki/Main_Page)