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



