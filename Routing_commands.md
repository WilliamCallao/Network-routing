

## ¿Qué es NAT?
Permite la traducción entre IP privadas y públicas. Mejora la seguridad y conserva IP públicas.

### Tipos de NAT:

1. **NAT Estática**: Traducción 1 a 1, útil para servidores internos.
2. **NAT Dinámica**: Asigna IP públicas temporales de un pool.
3. **PAT (NAT con Sobrecarga)**: Múltiples IP privadas comparten una IP pública usando puertos.

## Configuración de NAT:

### NAT Estática
```
Router(config)# ip nat inside source static DIR_IP_LOCAL DIR_IP_GLOBAL
Router(config)# interface Interfaz_red_local
Router(config-if)# ip nat inside
Router(config)# interface Interfaz_red_Global
Router(config-if)# ip nat outside
```

### NAT Dinámica
```
Router(config)# access-list NUM_LISTA permit DIR_RED wild_card
Router(config)# ip nat pool Nombre_Pool DRI_IP_INI DRI_IP_FIN netmask MASC_RED
Router(config)# ip nat inside source list NUM_LISTA pool Nombre_Pool
Router(config)# interface Interfaz_red_local
Router(config-if)# ip nat inside
Router(config)# interface Interfaz_red_Global
Router(config-if)# ip nat outside
```

### NAT con Sobrecarga (PAT)
```
Router(config)# access-list NUM_LISTA permit DIR_RED wild_card
Router(config)# ip nat inside source list NUM_LISTA interface Interfaz_red_Global overload
Router(config)# interface Interfaz_red_local
Router(config-if)# ip nat inside
Router(config)# interface Interfaz_red_Global
Router(config-if)# ip nat outside
```
