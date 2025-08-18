---
title: "Grundläggande CLI-kommandon"
parent: "Nätverk"
nav_order: 2270
---

# Grundläggande CLI-kommandon

### enable
Används för att logga in i enheten som administratör. Om du har konfigurerat användarnamn och lösenord får du fylla i det efteråt.
#### syntax:
enableExempel: Router>enable
### reload
Används för att starta om en enhet. Tänk på att alla kommandon du har lagt in kommer att nollställas, om du inte har sparat dem.
#### syntax:
reloadExempel: Router>reload
### show
Är ett “grundkommando” som används för att visa inställningar och/eller anslutna enheter till både switch och router.
#### syntax:
#### Exempel:  Router>show [vad du vill visa]Exempel:  Router>show interfaces statusExempel:  Router>show running-config
### exit
Används för att backa ur den nivå du befinner dig i. Om du har konfigurerat en port, och vill logga ut från det läget är detta kommandot du använder dig av
#### syntax:
exitExempel: Router (config-if)# exit
### configure terminal
Ändrar enhetens konfiguration, exempelvis portar m.m. Här behöver du vara för att göra alla inställningar.
#### syntax:
configure terminal eller conf tExempel: router#configure terminal eller Router#conf t
### hostname
Vi arbetar med många enheter i nätverket och något som är viktigt är att ha koll på vad de heter. Generellt döps routrar till R, och nummer i ordningen, till exempel: R1. Switchar döps på samma sätt och heter SW istället
#### syntax:
hostname [namn]Exempel: Router (config)#hostname R1
### interface
Används för att ansluta till en port och göra inställningar, brukar också skrivas int. Här är det vanligt att använda förkortningar för porten istället för portens hela namn.
#### syntax:
interface [portnamn]Exempel: Router (config)#interface GigabitEthernet0/0 eller:Router (config)#int g0/0
### shutdown
Används för att stänga av en port. Skrivs no framför blir det omvänt, dvs no shutdown blir: sätt på porten
#### syntax:
shutdown eller  shExempel för att stänga av: Router (config-if)#shutdown eller:Router (config-if)# sh
Exempel för att sätta på: Router (config-if)#no shutdown eller:Router (config-if)# no sh
### ip address
Används för att tilldela en IP-adress till porten. Vanligt att förkorta
#### syntax:
ip address [ip-adress subnätmask]eller  ip ad [ip-adress subnätmask]Exempel: Router (config-if)#ip address 192.168.0.1 255.255.255.0 eller:Router (config-if)#ip ad 192.168.0.1 255.255.255.0
### ip route
Används för att stänga skapa en statisk route, det vill säga hur trafiken går från en routers nätverk till en annan routers nätverk. Tänk på att du oftast måste göra en statisk route åt båda håll så att datorerna i det andra nätverket kan svara också.
#### syntax:
ip route [nätverksadress subnätmask next_hop]Exempel: Router (config)#ip route 192.168.0.0 255.255.255.0 10.0.0.1
### dhcp
Används för att skapa en dhcp-utdelning av ip-adresser. Den skapas i flera steg. Det första du anger är poolens namn. En pool är alla ip-adresser i ett subnät. Det andra du anger är nät-id för subnätet samt nätmask. Tredje saken är vilken gateway som nätverket skall ha. Avslutningsvis kan du (men är inget krav), lägga in DNS-serverns adress
#### syntax:
Router (config-if)#ip dhcp pool [poolnamn]
Router(dhcp-config)#network [nät-id] [subnätmask]
Router(dhcp-config)#default-router [gateway-ip]Router(dhcp-config)#dns-server [dns ip]Exempel:
Router (config-if)#ip dhcp pool polen
Router(dhcp-config)#network 192.168.0.0 255.255.255.0
Router(dhcp-config)#default-router 192.168.1.1
Router(dhcp-config)#dns-server 8.8.8.8
Precis som med ip-adresser, i ett VLAN, på en multilayerswitch, går det även att upprätta dhcp på en L3 switch. Kommandona är de samma, men du måste vara i VLAN-config-läge (se mer under rubriken VLAN)
### dhcp-avancerat - Ranges
Om du använder dig av DHCP kan du vilja ta bort vissa adresser eller ranges
#### syntax:
Router(dhcp-config)# ip dhcp excluded-address [start-IP] [slut-IP]
Exempel:
Router(dhcp-config)# ip dhcp excluded-address 192.168.0.2 192.168.0.9
### dhcp-avancerat - MAC-reservation
Om du använder dig av DHCP kan du vilja låsa en specifik mac-adress mot en viss ip
#### syntax:
Router(dhcp-config)# host [IP-adress] [subnetmask]Router(dhcp-config)# client-identifier [MAC-adress]
Exempel:
Router(dhcp-config)# host 192.168.0.1 255.255.255.0Router(dhcp-config)# client-identifier 0100.1A2B.3C4D.5E6F