# 10 - Mikrotik servidor DNS

 
```
/ip firewall filter add action=drop chain=input comment="drop_ataque_dns_udp" dst-port=53 in-interface=pppoe-brunosiqueira protocol=udp
/ip firewall filter add action=drop chain=input comment="drop_ataque_dns_tcp" dst-port=53 in-interface=pppoe-brunosiqueira protocol=tcp
```

```
/ip firewall nat add action=redirect chain=dstnat comment="focar_dns_local_udp" dst-port=53 in-interface=!pppoe-brunosiqueira protocol=udp to-ports=53
/ip firewall nat add action=redirect chain=dstnat comment="focar_dns_local_tcp" dst-port=53 in-interface=!pppoe-brunosiqueira protocol=tcp to-ports=53
```
 
 
## ou 
 
 
```
/ip firewall filter add action=drop chain=input comment=drop_ataque_dns_udp dst-port=53 in-interface=ether1 protocol=udp
/ip firewall filter add action=drop chain=input comment=drop_ataque_dns_tcp dst-port=53 in-interface=ether1 protocol=tcp
```

```
/ip firewall nat add action=redirect chain=dstnat comment=focar_dns_local_udp dst-port=53 in-interface=!ether1 protocol=udp to-ports=53
/ip firewall nat add action=redirect chain=dstnat comment=focar_dns_local_tcp dst-port=53 in-interface=!ether1 protocol=tcp to-ports=53
```