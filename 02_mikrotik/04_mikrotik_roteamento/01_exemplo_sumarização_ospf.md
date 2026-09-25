# Exemplo_sumarização_OSPF

```
/routing ospf area 
add area-id=0.0.0.1 name=PPPoE_Clientes
```

```
/routing ospf area range 
add area=PPPoE_Clientes range=10.250.2.0/24
```

```
/routing ospf network 
add area=PPPoE_Clientes comment=PPPoE_Clientes network=10.250.2.0/24
```