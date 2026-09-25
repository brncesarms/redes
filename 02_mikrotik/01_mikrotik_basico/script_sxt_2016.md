# SCRIPT-SXT-25-11-2016

## Este script contem algumas configurações básicas para SXT
```
/ip firewall nat 
add action=masquerade chain=srcnat log-prefix="" 
/interface wireless 
set [ find default-name=wlan1 ] antenna-gain=16 band=5ghz-onlyn country=brazil \ 
disabled=no frequency=5500 radio-name="obs colocar pppoe do cliente" ssid=\ 
FaarNet_Empresarial1-1 
/interface pppoe-client 
add add-default-route=yes disabled=no interface=wlan1 name=pppoe-cliente \ 
password=senha user=usuario 
/ip service 
set telnet disabled=yes 
set ftp disabled=yes 
set ssh disabled=yes 
set api disabled=yes 
set api-ssl disabled=yes 
/user 
add group=full name=faarnet password=linuxap 
/ip address 
add address=192.168.1.1/24 interface=ether1 network=192.168.1.0 
/ip dns 
set servers=186.219.240.34,186.219.240.35 
/ip pool 
add name=dhcp_pool1 ranges=192.168.1.2-192.168.1.254 
/ip dhcp-server 
add address-pool=dhcp_pool1 disabled=no interface=ether1 name=dhcp1 
/ip dhcp-server network 
add address=192.168.1.0/24 gateway=192.168.1.1 
/user 
remove admin 
```