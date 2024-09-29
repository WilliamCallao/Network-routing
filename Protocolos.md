## RIP (Routing Information Protocol)

```bash
enable
configure terminal
router rip
version 2
network <red_1>
network <red_2>
exit
write memory
```
## BGP (Border Gateway Protocol)

```bash
enable
configure terminal
router bgp <AS_local>
network <red_1> mask <máscara_1>
network <red_2> mask <máscara_2>
neighbor <IP_vecino> remote-as <AS_remoto>
exit
write memory
```

## OSPF (Open Shortest Path First)
```bash
enable
configure terminal
router ospf <ID_proceso>
network <red_1> <wildcard_mask_1> area <área_1>
network <red_2> <wildcard_mask_2> area <área_2>
exit
write memory
```






