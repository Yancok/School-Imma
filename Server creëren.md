# Server creëren
> Hier ga ik proberen een legite server creëren.  
> Alleen wanneer ik mij verveel werk ik hier aan negen van de tien.  
> Misschien later zet ik hem online ofzo.
  
## Wat is een server
Een server is een Dedicated Computer dat services geeft aan Clients bv Desktop Computers.  
Deze kunnen door het internet bereikt worden of in het Lokale netwerk.  
Een server kan 1 of meerdere doelen hebben zoals bv Web, Databasem, Email  
Een server is een rol dat een computer kreeg.  
Je kan een desktop omvormen naar een computer maar ze blijven gelimiteerd want je kan geen honderden mensen laten verbinden want het is niet gespecialiseerd ervoor.  
Servers moeten vertrouwbaar zijn. 
Server CPU voorbeeld Intel Xeon.  
Xeon support dan ook de ECC RAM (Error-Correcting Code) wat een normale CPU niet doet.  
ECC RAM checkt data voor memory errors die mogelijk een server neerhalen en die voorkomen. blijkbaar support AMD CPU's deze RAM wel maar intel niet.  
> RAID of `Redundant Array of Independent Disks` zorgt ervoor dat dezelfde data over 2 harde schijfen staat geschreven tegelijk zodat als 1 schijf kapot gaat je nog een backup hebt van de andere harde schijf.  

Server OS moeten krachtig en stabiel zijn.
Types Servers|Doel|
|--|--|
Web server| Host een website, de Server behoudt al de data van de website en code.|
Email Server|Stuurt of krijgt email door u webbrowser of door een email client.|
Database| Bewaard data in de backend en haalt ze terug op in de Frontend bv SQL.|
---
## IP uitleg  
Een IP Adress is een `identificatie`  van een Computer of Apparaat op een *Netwerk*.  
Elke apparaat heeft er een voor communicatie bedoelingen.  
 
***IPv4***  
Een IPv4 Adress is een 32-bit adress geschreven als 4 nummer groepen gedeeld door periods.  
Elk nummer groep dat door periods `.` verdeeld zijn noemt een **Octet**.  
Deze nummers vallen tussen de 0-255.  
Een IP address bestaad uit 2 delen een `Network address` en een `Host address`.  
Een Network address is een address dat aan een heel Network is gegeven.  
De Host Address is het address dat gegeven is aan de Hosts in dat Network bv. Computers, servers, tablets, routers  
Dus iedereen heeft een *uniek* Host address.  
Om te weten welk deel van het IP address de Network en Host is gebruik je een Subnet Mask.  
Een subnet Mask is iets wat op de IP address lijkt, Het weergeeft hoeveel `bits` in het IP address er gebruikt wordt door het netwerkgedeelte van het IP-adres te maskeren.  
  
IP address en Subnet Mask zijn nutteloos in hun `Decimal Format` want computers en Netwerken lezen die niet u dat formaat.  
Ze lezen die alleen in een `Binary Format`, Om deze te krijgen kijk je naar de 8-Bit Octet Chart.  
  
***8-Bit Octet Chart***
128|64 |32 |16 |8  |4  |2  |1  |  
|---|---|---|---|---|---|---|---|  
  
Je schrijft 1 onder de nummers die u Octet namaken.  
> bv. 192.168.1.0 ----> 11000000.10101000.00000001.00000000 is de Binary Format van het IP address  
> En 255.255.255.0 -->  11111111.11111111.11111111.00000000 is de Binary Format van het Subnet Mask 
 
Dus om te weten welk deel het IP address is wanneer de Subnet masks binary 1's overeen komen met de IP address binary is het een Network address en de overige een Host address.  
> `11000000.10101000.00000001`.00000000 Dus de ` ` is een Network address en de nullen is de Host Address.    
> `11111111.11111111.11111111`.00000000   

### Subnetting
Subnetting is een Netwerk verdelen in kleiner netwerken door de hulp van routers om de drukte te verminderen.  
Om een aan subnetting te doen is door het *veranderen* van de Default Subnet Mask door te lenen van bits van de Host Address.  
> Bijvoorbeeld:  
> `11111111`.`11111111`.`11111111`.00000000 heeft 1 Netwerk en 254 hosts (Subnet Mask: 255.255.255.0).  
> `11111111`.`11111111`.`11111111`.`1`0000000 Heeft 2 Netwerken en 126 Hosts (Subnet Mask: 255.255.255.128).   
> `11111111`.`11111111`.`11111111`.`11`000000 Heeft 4 Netwerken en 62 Hosts (Subnet Mask: 255.255.255.192).  
> ... Enzo verder  
> `11111111`.`11111111`.`11111111`.`111111`00 Is de limiet want dan heb je 64 Netwerken met 2 Hosts (Subnet Mask: 255.255.255.252).  

Er is nog meer aan Subnetting maar dit zijn de basics.  
Er zijn ook Classes zoals volgt.  
Class|First Octet Address|Default Subnet Mask|Ongeveer mogelijke Hosts|
---|---|---|--|
A|1-126|255.0.0.0|16 miljoen hosts|
B|128-191|255.255.0.0|65.000 hosts|
C|192-223|255.255.0.0|254 hosts|  
 
### CIDR  
CIDR - Classless Inter-Domain Routing  
  
Of wel bekend als Slash Notation, is wanneer je een Subnet Mask geeft met een slash erachter waar de hoeveelheid 1's erin zitten in de subnet mask.  
> bv 192.168.1.0 /24 dat betekent dat de Subnet mask 24-bit lengte is, dus 24 1's.  

### NAT
NAT - Network Address Translation  

Neemt meerdere addressen in u netwerk en geeft 1 IP Address aan het internet waardoor het gebruik van de wereldwijde IP addressen verminderd wordt.  

---
## Ubuntu Server
Klik de link naar de Ubuntu Server site en ga naar Option 2 en download de .iso.  
Install u .iso bestand in de VM en volg de stappen van de OS.  
Vul al de dingen die u wilt in en wacht tot de installatie klaar is.  
> ***WEES ZEKER DAT NETWERK AAN STAAT BIJ DE INSTELLINGEN VAN DE VM***  
  
Configure u taal en toetsenbord.  
Network connections 

---
## NAS maken
> Network Attached Storage maken van een oude Laptop die niet meer gebruikt wordt.  
> En later om te zetten in mischien een Minecraft server.  
### Virtuele NAS maken
> want ik ben wil eerste virtueel proberen voor dat ik iets op fuck lol  

---
## Alles links die gebruikt worden:
* [Uitleg wat een server is `simpel`](https://www.youtube.com/watch?v=UjCDWCeHCzY&list=WL&index=9)
* [Your Old PC is Your New Server, Linus techtips](https://youtu.be/zPmqbtKwtgw?list=PL8IHkci_kZpA6lGtS4jpvIFFe8l7eqO3i)
* [Download Ubuntu Server.iso](https://ubuntu.com/download/server)
* [Verschillen tussen Ubuntu Desktop en Server](https://youtu.be/sJjEzek2e6I)
* [Setup Dedicated Home File Server](https://www.youtube.com/watch?v=RDwoDj2cW6c)
* [TrueNAS ](https://www.truenas.com/) 
* [How to Create a NAS with Ubuntu Server](https://www.youtube.com/watch?v=-5Z_-3EBIHE&list=PL8IHkci_kZpA6lGtS4jpvIFFe8l7eqO3i&index=128) & [Documentatie](https://quidsup.net/tutorials/?p=ubuntu-create-nas#2-installing)  --> Ubuntu NAS server
