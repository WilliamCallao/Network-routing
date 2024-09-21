
# Enrutamiento y Configuración de VLANs

## Configuración en Switch

```
# vlan id_vlan
# name name_vlan
# exit
```

### Asignar Rango de Interfaces

```
# interface range fa0/1-5
# switchport mode access
# switchport access vlan id_vlan
# exit
```

### Configuración de Trunk

```
# interface fa0/24
# switchport mode trunk
# exit
```

## Asignar IPs a Routers (Subinterfaces)

```
# interface fa0/0.5
# encapsulation dot1Q 10
# ip address 192.168.5.1 255.255.255.0
# exit

# interface fa0/0.25
# encapsulation dot1Q 20
# ip address 192.168.25.1 255.255.255.0
)# exit

# interface fa0/0
# no shutdown
# exit
```

