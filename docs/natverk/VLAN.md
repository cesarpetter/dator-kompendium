---
title: "VLAN"
parent: "Nätverk"
nav_order: 2280
---

# VLAN

Skapar ett virtuellt nätverk på en port, så kallade sub-portar. VLAN standard är att de döps till jämnt 10-tal
#### syntax:
int [portnamn.vlan-id]encapsulation dot1q [vlanid]
Exempel: Router (config)#int g0/0.10 Router(config-subif)# encap dot1q 10
Om du utför detta på en multilayerswitch behöver du inte skapa vare sig subport eller encapsulation. Där räcker det med att du skapar VLAN och tilldelar portar
#### syntax:
[vlan-id]name [vlan-name]
Switch(config)#vlan 10
Switch(config-vlan)#name vlan-name
Exempel: Switch(config)#vlan 10 Switch(config-vlan)# name vlan10
Därefter måste du fortfarande tilldela portar (enligt nedan), ip adresser, dhcp m.m.
### switchport
Används på switch för att hantera VLAN. Porten ställs antingen som access eller trunk. En trunk-port har hand om all trafik från samtliga VLAN och är ofta den port som leder tillbaka till routern. Access är den port som enheter ansluter till.
#### syntax:
switchport mode [typ av anslutning]Exempel trunk: Switch(config-if)#switchport mode trunk Exempel access: Switch(config-if)#switchport mode access Switch(config-if)#switchport access vlan 10
Skall du göra flera portar samtidigt kan du använda kommandot int range [startport-slutport]
### ip routing
Vill du låta din multilayerswitch hantera trafiken måste du aktivera intern routing i den
#### syntax:
ip routingExempel: Switch(config)#ip routing