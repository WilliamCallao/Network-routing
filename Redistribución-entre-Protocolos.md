## Redistribución entre Protocolos

### Redistribución de RIP a BGP

```bash
enable
configure terminal
router rip
version 2
default-information originate
exit
router bgp <AS_local>
redistribute connected
network <red_no_conectada_1> mask <máscara_1>
network <red_no_conectada_2> mask <máscara_2>
exit
write memory
```
### Redistribución de BGP a OSPF

```bash
enable
configure terminal
router bgp <AS_local>
redistribute ospf <ID_proceso>
exit
router ospf <ID_proceso>
redistribute bgp <AS_local> subnets
default-information originate
exit
write memory
```
