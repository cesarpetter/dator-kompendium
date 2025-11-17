---
title: "Kodsnipplets att använda"
parent: "Nätverk"
nav_order: 2260
---

# Kodsnipplets att anvanda

## Sammanfattning
När vi jobbar med nätverkskonfiguration handlar mycket av arbetet om planering, kontroll och felsökning. Är det något som inte fungerar, kontrollera paketets väg, från början till slut för att se var det har blivit fel.
Ta ALLTID för vana att placera ut saker organiserat och döp allting med exempelvis ip-adresser eller korrekta hostnames. Även det kommer göra felsökningen mycket enklare.
Många av de kommandon som används skrivs sällan ut som hela kommandon, då du kan använda förkortningar istället. Ofta när du söker hjälp på google m.m. så kommer förkortningarna upp. Exempel på detta är när du ansluter till en port eller skall sätta på en port. I de fallen skrivs bara förkortningar till kommandot ut.
Den första fråga du får när du ansluter till enheten är: Would you like to enter the initial configuration dialog? [yes/no], där svarar vi ALLTID no.
Att använda sig av ett frågetecken, ?, listar alla tänkbara kommandon som finns på nivån eller som fortsättning på kommandot du matat in.
För att avbryta pågående kommando trycker du Ctrl+Shift+6.
Det sista tipset är att alltid ansluta en dator till enheten som du skall konfigurera. Detta för att minimera risken att du råkar göra ändringar i portinställningarna på enheten.
Lycka till.

## Grundlaggande CLI-kommandon

### enable
Används för att logga in i enheten som administratör. Om du har konfigurerat användarnamn och lösenord får du fylla i det efteråt.
#### syntax:
enable
Exempel: Router>enable

### reload
Används för att starta om en enhet. Tänk på att alla kommandon du har lagt in kommer att nollställas, om du inte har sparat dem.
#### syntax:
reload
Exempel: Router>reload

### show
Är ett “grundkommando” som används för att visa inställningar och/eller anslutna enheter till både switch och router.
#### syntax:
Exempel: Router>show [vad du vill visa]
Exempel: Router>show interfaces status
Exempel: Router>show running-config

### exit
Används för att backa ur den nivå du befinner dig i. Om du har konfigurerat en port, och vill logga ut från det läget är detta kommandot du använder dig av.
#### syntax:
exit
Exempel: Router (config-if)# exit

### configure terminal
Ändrar enhetens konfiguration, exempelvis portar m.m. Här behöver du vara för att göra alla inställningar.
#### syntax:
configure terminal eller
conf t
Exempel: router#configure terminal eller
Router#conf t

### hostname
Vi arbetar med många enheter i nätverket och något som är viktigt är att ha koll på vad de heter. Generellt döps routrar till R, och nummer i ordningen, till exempel: R1. Switchar döps på samma sätt och heter SW istället.
#### syntax:
hostname [namn]
Exempel: Router (config)#hostname R1

### interface
Används för att ansluta till en port och göra inställningar, brukar också skrivas int.
#### syntax:
interface [portnamn]
Exempel:
Router (config)#interface GigabitEthernet0/0
eller:
Router (config)#int g0/0

### shutdown
Används för att stänga av en port. Skrivs no framför blir det omvänt.
#### syntax:
shutdown eller sh
Exempel för att stänga av:
Router (config-if)#shutdown
eller:
Router (config-if)# sh
Exempel för att sätta på:
Router (config-if)#no shutdown
eller:
Router (config-if)# no sh

### ip address
Används för att tilldela en IP-adress till porten.
#### syntax:
ip address [ip-adress subnätmask]
eller
ip ad [ip-adress subnätmask]
Exempel:
Router (config-if)#ip address 192.168.0.1 255.255.255.0
eller:
Router (config-if)#ip ad 192.168.0.1 255.255.255.0

### ip route
Används för att skapa en statisk route.
#### syntax:
ip route [nätverksadress subnätmask next_hop]
Exempel:
Router (config)#ip route 192.168.0.0 255.255.255.0 10.0.0.1

### dhcp
Används för att skapa en DHCP-pool.
#### syntax:
ip dhcp pool [poolnamn]
network [nät-id] [subnätmask]
default-router [gateway-ip]
dns-server [dns ip]

Exempel:
ip dhcp pool polen
network 192.168.0.0 255.255.255.0
default-router 192.168.1.1
dns-server 8.8.8.8

### DHCP – ranges
syntax:
ip dhcp excluded-address [start-IP] [slut-IP]

### DHCP – MAC-reservation
syntax:
host [IP-adress] [subnetmask]
client-identifier [MAC-adress]

## DYNAMISKA ROUTINGPROTOKOLL

### RIP v2
router rip
v 2
network [IP för anslutning]
network [IP för LAN som delas ut]
no auto-summary

### OSPF
router ospf [process-id]
network [IP] [Wildcardmask] area [nummer]

### Cost
interface [port]
ip ospf cost [värde]

## VLAN
int [portnamn.vlan-id]
encapsulation dot1q [vlanid]

Exempel:
int g0/0.10
encap dot1q 10

På MLS:
vlan-id
name [vlan-name]

switchport mode trunk
switchport mode access
switchport access vlan 10

int range [start-slut]

### ip routing
ip routing

## Kommandon i Windows
ipconfig
Kommando för att se dina nätverksanslutningar.

ipconfig /all
Fullständig info.

ipconfig /release
Släpper IP-adress.

ipconfig /renew
Begär ny IP.

ipconfig /displaydns
Visar DNS-cache.

ipconfig /flushdns
Tömmer DNS-cache.

nslookup
Ger information om domännamn och IP-adresser.
Syntax:
nslookup google.com

ping
Skickar ICMP.
Syntax:
ping 192.168.0.1

tracert
Visar hur trafiken routras.
Syntax:
tracert 192.168.0.1

## Kommandon i Linux (Debian)
ip -brief addr
Kommando för att snabbt se aktiva nätverksgränssnitt.

ip addr show
Detaljerad info.

ip link show
Visar länkstatus.

ip route show
Visar routningstabellen.
Syntax:
ip route show
ip route get 192.168.0.1

dhclient -r
Släpper DHCP-lease.
Syntax:
sudo dhclient -r -v eth0

dhclient
Begär ny DHCP-lease.
Syntax:
sudo dhclient -v eth0

resolvectl status
Visar DNS-resolver-info.
Syntax:
resolvectl status
resolvectl query google.com
resolvectl flush-caches

dig
Ger DNS-info.
Syntax:
dig +short google.com
dig -x 192.168.0.1 +short

ping
Testar anslutning.

tracepath
Hop-för-hop-väg utan root.

mtr
Kombinerar ping och traceroute.
Syntax:
mtr google.com
mtr -6 2607:f8b0:4003:c00::6a
