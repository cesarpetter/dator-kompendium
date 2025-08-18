# Appendix II - CLI-REFERENS

## VLAN

Skapar ett virtuellt nätverk på en port, så kallade sub-portar. VLAN standard är att de döps till jämnt 10-tal

#### syntax:

int [portnamn.vlan-id]
encapsulation dot1q [vlanid]

Exempel: Router (config)#int g0/0.10
Router(config-subif)# encap dot1q 10

Om du utför detta på en multilayerswitch behöver du inte skapa vare sig subport eller encapsulation. Där räcker det med att du skapar VLAN och tilldelar portar

#### syntax:

[vlan-id]
name [vlan-name]

Switch(config)#vlan 10

Switch(config-vlan)#name vlan-name

Exempel: Switch(config)#vlan 10
Switch(config-vlan)# name vlan10

Därefter måste du fortfarande tilldela portar (enligt nedan), ip adresser, dhcp m.m.

### switchport

Används på switch för att hantera VLAN. Porten ställs antingen som access eller trunk. En trunk-port har hand om all trafik från samtliga VLAN och är ofta den port som leder tillbaka till routern. Access är den port som enheter ansluter till.

#### syntax:

switchport mode [typ av anslutning]
Exempel trunk: Switch(config-if)#switchport mode trunk
Exempel access: Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 10

Skall du göra flera portar samtidigt kan du använda kommandot int range [startport-slutport]

### ip routing

Vill du låta din multilayerswitch hantera trafiken måste du aktivera intern routing i den

#### syntax:

ip routing
Exempel: Switch(config)#ip routing


ipconfig

Kommando för att se dina nätverksanslutningar i datorn. Den visar alla olika, ethernet, wlan, bluetooth m.m. Alla med en enkel översikt över ip adress m.m.

ipconfig /all

Kommando för att se dina nätverksanslutningar i datorn men, all information. Den visar alla olika, ethernet, wlan, bluetooth m.m. Alla med en enkel översikt över ip adress m.m.

ipconfig /release

Kommando för att släppa den ip-adress du har blivit tilldelad

ipconfig /renew

Kommando för att begära ny ip-adress

ipconfig /displaydns

Visar innehållet i DNS-cache

ipconfig /flushdns

Töm innehållet i DNS-cache

nslookup

Ger information om domännamn och ip-adresser

Syntax:

nslookup google.com

ping

Skickar ett ICMP-paket till en specifik ip adress, i syfte att kontrollera anslutningen

Syntax:

ping 192.168.0.1

tracert

Visar hur nätverkstrafiken routras till en viss ip. Du kan även (om du är ansluten till en DNS) skriva in en URL (webbadress)

Syntax:

tracert 192.168.0.1

ip -brief addr
Kommando för att snabbt se aktiva nätverksgränssnitt och deras IP-adresser (kompakt översikt).

ip addr show
Kommando för att se dina nätverksgränssnitt i detalj: IPv4/IPv6-adresser, prefix, flags m.m.

ip link show
Visar länkstatus, MAC-adresser och MTU per interface (lager 2-vy).

ip route show
Visar routningstabellen (standardgateway, statiska rutter m.m.).
Syntax:
ip route show
ip route get 192.168.0.1

dhclient -r
Kommando för att släppa (release) din DHCP-lease på ett interface.
Syntax:
sudo dhclient -r -v eth0

dhclient
Kommando för att begära en ny DHCP-lease (renew) på ett interface.
Syntax:
sudo dhclient -v eth0

resolvectl status
Visar DNS-resolvrar och cache-statistik om systemd-resolved används.
Syntax:
resolvectl status
resolvectl query google.com

resolvectl flush-caches
Tömmer DNS-cache (gäller systemd-resolved; annars töm respektive cache-tjänst).

dig
Ger detaljerad information om domännamn och IP-adresser (ersätter ofta nslookup).
Syntax:
dig +short google.com
dig -x 192.168.0.1 +short

ping
Skickar ICMP-ekon till en adress för att testa anslutning och rundtid.

tracepath
Visar vägen (hop för hop) som paket tar till en destination, utan root-krav.

mtr
Kombinerar ping och traceroute i realtid (fördröjning/förluster per hop). Kan behöva installeras (sudo apt install mtr).
Syntax:
mtr google.com
mtr -6 2607:f8b0:4003:c00::6a


