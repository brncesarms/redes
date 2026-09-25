# 3 - NAT

```
/ip firewall nat add action=masquerade chain=srcnat comment=Full-masquerade
```
 
## ou

```
/ip firewall nat add action=masquerade chain=srcnat comment=Mascaramento out-interface=ether1
```