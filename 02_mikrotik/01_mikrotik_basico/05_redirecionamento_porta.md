# 5 - Redirecionamento porta

```
/ip firewall nat add action=dst-nat chain=dstnat comment="rota vnc CAIXA1" dst-port=39803 protocol=tcp to-addresses=192.168.10.3 to-ports=5900
```
 
## ou 

```
/ip firewall nat add action=dst-nat chain=dstnat comment="CAMERAS SERVER" dst-address=177.11.164.10 to-addresses=192.168.2.3
```