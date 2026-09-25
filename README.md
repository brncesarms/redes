---
title: "Network Engineering, Routing & MikroTik RouterOS v7 Runbooks"
date_created: 2024-02-25
author: "Bruno César / Antigravity"
privacy: public
tags:
  - publico
  - redes
  - mikrotik
  - routeros
  - tcp-ip
  - ospf
  - ubiquiti
  - tailscale
  - devops
---

# 🌐 Network Engineering, Routing & MikroTik RouterOS v7

[![Platform](https://img.shields.io/badge/RouterOS-MikroTik%20v7-E01A22?logo=mikrotik&logoColor=white)](#)
[![Protocol](https://img.shields.io/badge/Routing-OSPF%20%7C%20BGP%20%7C%20Static-0052CC)](#)
[![Security](https://img.shields.io/badge/Firewall-Stateful%20%7C%20FastTrack-red)](#)
[![VPN](https://img.shields.io/badge/VPN-Tailscale%20%7C%20WireGuard%20%7C%20OpenVPN-4EAA25)](#)
[![Lab](https://img.shields.io/badge/Lab%20Emulation-EVE--NG%20%7C%20PNetLab-blueviolet)](#)
[![Obsidian](https://img.shields.io/badge/Knowledge%20Base-Obsidian-483699?logo=obsidian&logoColor=white)](#)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](#)

> [!NOTE]
> **Repositório Oficial de Engenharia de Redes & Conectividade**  
> Runbooks operacionais, configurações de alta performance para MikroTik RouterOS v7, roteamento dinâmico (OSPF), segmentação CIDR, hardening de firewall de borda, enlaces wireless e malhas seguras VPN com Tailscale e WireGuard.

---

## 🎯 Visão Geral & Filosofia de Infraestrutura

Este repositório consolida padrões de projeto, templates determinísticos e procedimentos operacionais para redes corporativas e provedores de conectividade. O foco é estabelecer **topologias escaláveis, seguras e com mínimo consumo de recursos computacionais**, priorizando funcionalidades modernas do **RouterOS v7** (L3 Hardware Offloading, FastTrack, WireGuard nativo e automação via SSH/API).

---

## 📚 Catálogo Temático dos Runbooks

### 🌐 1. Fundamentos de Redes, IPv4 & Wi-Fi
| Runbook | Descrição | Tecnologias |
| :--- | :--- | :--- |
| [**01. IPs de Rede Interna**](01_redes_basico/01_ips_rede_interna.md) | Classes RFC 1918, blocos CIDR (/24 a /28) e boas práticas de dimensionamento. | `IPv4`, `CIDR`, `Subnetting` |
| [**02. Fundamentos de Redes Wi-Fi**](01_redes_basico/02_redes_wifi.md) | Propagação de RF, bandas 2.4/5 GHz e boas práticas em ambientes corporativos. | `Wi-Fi 802.11`, `RF` |

### ⚙️ 2. MikroTik RouterOS: Serviços Essenciais & Hardening
| Runbook | Descrição | Módulos RouterOS |
| :--- | :--- | :--- |
| [**01. IP, DNS, Pool e Servidor DHCP**](02_mikrotik/01_mikrotik_basico/01_ip_dns_pool_dhcp.md) | Provisionamento de IP de gateway, servidores DNS e escopo DHCP. | `/ip address`, `/ip dhcp-server` |
| [**02. Gerenciamento de Usuário e Senha**](02_mikrotik/01_mikrotik_basico/02_alterando_usuario_senha.md) | Criação de contas administrativas seguras e revogação de acessos padrão. | `/user` |
| [**03. Configuração de Source NAT (Masquerade)**](02_mikrotik/01_mikrotik_basico/03_nat.md) | Regras de mascaramento de tráfego para saída de estações locais à Internet. | `/ip firewall nat` |
| [**04. Zona Desmilitarizada (DMZ)**](02_mikrotik/01_mikrotik_basico/04_dmz.md) | Isolamento e encaminhamento para servidores públicos em DMZ dedicada. | `/ip firewall nat` |
| [**05. Redirecionamento de Portas (Dst-NAT)**](02_mikrotik/01_mikrotik_basico/05_redirecionamento_porta.md) | Encaminhamento de portas externas para serviços internos específicos. | `/ip firewall nat` |
| [**06. Desativação de Serviços Inseguros**](02_mikrotik/01_mikrotik_basico/06_desativar_telnet_ssh_ftp_api.md) | Redução de superfície de ataque desativando Telnet, FTP e APIs não utilizadas. | `/ip service` |
| [**07. Bloqueio de Sites e Serviços**](02_mikrotik/01_mikrotik_basico/07_bloqueio_sites_servicos.md) | Filtragem por DNS estático e listas de bloqueio no firewall. | `/ip firewall filter` |
| [**08. Priorização de Tráfego & QoS**](02_mikrotik/01_mikrotik_basico/08_priorizar_sites_e_servicos.md) | Marcação de pacotes e conexões (Mangle) para priorização de tráfego crítico. | `/ip firewall mangle` |
| [**09. Controle de Banda por IP (Simple Queues)**](02_mikrotik/01_mikrotik_basico/09_controle_de_banda_por_ip.md) | Definição de limites de taxa de upload/download por host ou subnet. | `/queue simple` |
| [**10. Servidor DNS Cache no MikroTik**](02_mikrotik/01_mikrotik_basico/10_servidor_dns_mikrotik.md) | Cache DNS local acelerado com suporte a requisições remotas controladas. | `/ip dns` |
| [**11. Habilitação de RoMON (Layer 2)**](02_mikrotik/01_mikrotik_basico/11_habilitar_romon.md) | Gerenciamento de múltiplos dispositivos MikroTik sem necessidade de IP direto. | `/tool romon` |
| [**12. Acesso SSH via Terminal Linux**](02_mikrotik/01_mikrotik_basico/12_acesso_ssh_mikrotik_via_terminal_linux.md) | Automação e administração CLI com chaves SSH sem solicitação de senha. | `/user ssh-keys` |
| [**13. Template de Provisionamento SXT/CPE**](02_mikrotik/01_mikrotik_basico/13_script_sxt_2016.md) | Script de configuração padrão para estações clientes e pontes de rádio. | `System Script` |
| [**14. Reboot Automático Programado**](02_mikrotik/01_mikrotik_basico/14_automatic_reboot.md) | Rotina de reinicialização preventiva agendada via Scheduler. | `/system scheduler` |

### 🛡️ 3. Firewall Stateful & Segurança de Borda
| Runbook | Descrição | Módulos RouterOS |
| :--- | :--- | :--- |
| [**01. Proteção Básica de Firewall Stateful**](02_mikrotik/02_mikrotik_firewall/01_basico_para_proteger_seu_mikrotik.md) | Filtragem de tráfego inválido, proteção da chain input e aceleração FastTrack. | `/ip firewall filter` |

### 🔀 4. Roteamento Dinâmico & Emulação de Laboratórios
| Runbook | Descrição | Tecnologias |
| :--- | :--- | :--- |
| [**01. Sumarização de Rotas no OSPF**](02_mikrotik/04_mikrotik_roteamento/01_exemplo_sumarizacao_ospf.md) | Engenharia de tráfego, agregação de sub-redes e redução de LSAs no OSPF. | `/routing ospf` |
| [**01. MikroTik RouterOS no EVE-NG**](02_mikrotik/03_mikrotik_eve_ng/01_eve_ng.md) | Provisionamento de imagens CHR paravirtualizadas em topologias virtuais EVE-NG. | `EVE-NG`, `QEMU`, `CHR` |

### 📡 5. Wireless Enlaces & Infraestrutura Ubiquiti
| Runbook | Descrição | Tecnologias |
| :--- | :--- | :--- |
| [**01. Canais Regulamentados Brasil 5 GHz**](02_mikrotik/05_mikrotik_wireless/01_canais_brasil_5ghz.md) | Tabela regulatória Anatel de frequências e potências para enlaces 5 GHz. | `Wireless`, `Anatel 5GHz` |
| [**02. Análise Espectral (Spectral Scan)**](02_mikrotik/05_mikrotik_wireless/02_analise_espectral.md) | Varredura de RF e diagnóstico de interferência via rádio MikroTik. | `/interface wireless spectral` |
| [**01. Remoção de Malware Skynet em Ubiquiti**](03_ubiquiti/01_removendo_skynet.md) | Limpeza, expurgo de scripts maliciosos e restauração de firmware airOS. | `Ubiquiti`, `airOS`, `SSH` |

### 🔒 6. Malhas VPN, Tailscale & Conectividade Corporativa
| Runbook | Descrição | Tecnologias |
| :--- | :--- | :--- |
| [**01. Arquitetura de Rede, Tailscale & VPN MikroTik**](04_vpn_tailscale/01_arquitetura_tailscale_vpn_mikrotik.md) | Guia completo de malha privada Tailscale/WireGuard e VPNs para clientes MikroTik. | `Tailscale`, `WireGuard`, `MikroTik` |

---

## 🛠️ Como Utilizar este Repositório

### Clonagem Local
```bash
git clone git@github.com:brncesarms/redes.git
cd redes
```

### Visualização Recomendada
- **Obsidian**: Abra o diretório como cofre técnico para navegar pela teia de conhecimentos e referências cruzadas entre roteamento, firewall e serviços.
- **Terminal & WinBox**: Os scripts e blocos de comandos RouterOS podem ser colados diretamente no terminal do WinBox ou enviados via sessão SSH remota.

---

## 🤝 Conexão com a Caixa de Ferramentas Multiplataforma

Automações e scripts relacionados a testes de rede, rotinas SSH e integração com o ecossistema da bancada estão disponíveis em:
🔗 **[Repositório brncesarms/scripts](https://github.com/brncesarms/scripts)**

---

## 👤 Autor

**Bruno César**  
*Engenheiro de Infraestrutura, Redes & Automação*  
- **GitHub**: [@brncesarms](https://github.com/brncesarms)
- **LinkedIn**: [linkedin.com/in/brncesarms](https://linkedin.com/in/brncesarms)