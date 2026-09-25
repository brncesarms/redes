# 8 - Priorizar - SITE e SERVIÇOS

```
/ip firewall mangle 
add action=add-dst-to-address-list address-list=Lista-IPTV address-list-timeout=1d chain=prerouting content=tv5.cs10.tv src-address=192.168.11.0/24 
add action=mark-connection chain=prerouting dst-address-list=Lista-IPTV new-connection-mark=tv-conexoes passthrough=yes 
add action=mark-packet chain=prerouting connection-mark=tv-conexoes new-packet-mark=tv-pacotes passthrough=yes
```

```
/queue tree 
add limit-at=3M max-limit=3M name=IPTV packet-mark=tv-pacotes parent=global priority=1
```