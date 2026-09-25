# 4 - DMZ

``` 
/ip firewall nat add action=dst-nat chain=dstnat dst-address=186.219.242.3 dst-port=!8291 protocol=tcp to-addresses=192.168.1.4 to-ports=0-65535
```
 
 
## ou   
 
```
/ip firewall nat add action=dst-nat chain=dstnat dst-port=!8291 protocol=tcp to-addresses=192.168.1.4 to-ports=0-65535
```