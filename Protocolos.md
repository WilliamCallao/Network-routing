# Manual de Protocolos de Enrutamiento

Este archivo contiene los comandos esenciales para configurar los protocolos de enrutamiento RIP, BGP y OSPF en dispositivos Cisco.

---

## Protocolo RIP (Routing Information Protocol)

RIP es un protocolo de enrutamiento basado en la distancia que utiliza la métrica de saltos (hops) para determinar la mejor ruta.

### Configuración de RIP

1. Entra en modo privilegiado:
    ```
    > enable
    ```

2. Entra en el modo de configuración global:
    ```
    # configure terminal
    ```

3. Activa el protocolo RIP:
    ```
    (config)# router rip
    ```

4. Configura la versión 2 de RIP:
    ```
    (config-router)# version 2
    ```

5. Define las redes que participan en RIP (solo red, sin máscara):
    ```
    (config-router)# network [red]
    ```

6. Sal del modo de configuración del router:
    ```
    (config-router)# exit
    ```

---

## Protocolo BGP (Border Gateway Protocol)

BGP es un protocolo de enrutamiento exterior utilizado en sistemas autónomos para intercambiar información de enrutamiento en internet.

### Configuración de BGP

1. Entra en modo privilegiado:
    ```
    > enable
    ```

2. Entra en el modo de configuración global:
    ```
    # configure terminal
    ```

3. Activa BGP y define el número del sistema autónomo (AS):
    ```
    (config)# router bgp [AS propio]
    ```

4. Anuncia una red a BGP (incluyendo la máscara):
    ```
    (config-router)# network [red] mask [máscara]
    ```

5. Define un vecino (neighbor) y su AS remoto:
    ```
    (config-router)# neighbor [IP del vecino] remote-as [AS del vecino]
    ```

6. Sal del modo de configuración del router:
    ```
    (config-router)# exit
    ```

---

## Protocolo OSPF (Open Shortest Path First)

OSPF es un protocolo de enrutamiento interior basado en el estado de enlaces y utiliza áreas para organizar las redes.

### Configuración de OSPF

1. Entra en modo privilegiado:
    ```
    > enable
    ```

2. Entra en el modo de configuración global:
    ```
    # configure terminal
    ```

3. Activa OSPF y asigna un proceso de enrutamiento (número arbitrario):
    ```
    (config)# router ospf [ID proceso]
    ```

4. Configura una red con su wilcard y área de OSPF:
    ```
    (config-router)# network [red] [wilcard] area [número de área]
    ```

5. Sal del modo de configuración del router:
    ```
    (config-router)# exit
    ```

