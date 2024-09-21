
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
