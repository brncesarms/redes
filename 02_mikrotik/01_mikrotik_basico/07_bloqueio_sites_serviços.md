# 7 - Bloqueio: SITES e SERVIÇOS

```
/ip firewall address-list add address=192.168.10.30 list="Fora do bloqueio do Youtube"
```
 
```
/ip firewall filter add action=drop chain=forward comment="Bloqueio Youtube" content=youtube src-address=192.168.10.0/27 src-address-list="!Fora do bloqueio do Youtube"
```