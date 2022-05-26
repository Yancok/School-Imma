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
## Bestanden delen over een Netwerk (Windows 10)  
### Computer klaarmaken voor Bestanden Deling:
Stap |***Uitleg*** | Foto|
---|---|---|
1.| Open Instellingen en ga naar`Network en Internet`|![image](https://user-images.githubusercontent.com/105280571/170562910-2512e323-2023-459d-bca7-0c9139d2106b.png) |
2.| Verander Public Network naar Private Network door op `Eigenschappen` te klikken | ![image](https://user-images.githubusercontent.com/105280571/170563411-d4bc6b2d-ad92-408c-ae23-17e7e05ea455.png)|
3.| Verander het naar `Prive` | ![image](https://user-images.githubusercontent.com/105280571/170563648-523326c6-1f65-4919-9f0a-4f21406fac43.png) |
4.| Ga 2 keer terug met het pijltje links bovenaan en scroll naar benen en klik op `Netwerk Centrum`| ![image](https://user-images.githubusercontent.com/105280571/170564062-75b44786-6895-446b-b2f0-07a6118fe8fe.png) |
5.| Klik op `Geavanceerde instellingen voor delen wijzigen`| ![image](https://user-images.githubusercontent.com/105280571/170564777-7b21b1f4-ffd1-48fe-a224-757405c57486.png) |
6.| Zet u Bestanden deling optie aan | ![image](https://user-images.githubusercontent.com/105280571/170565056-6d39d03d-f08e-4757-9528-b318302b9984.png)| 
7.| Zet u Public folders open aan iedereen en als u problemen heeft kan het liggen aan u verbinding encriptie probeer deze op 40 of 56-bits te zetten dit kan alleen voorkomen als u andere apparatuur te oud is en niet de 128-bit encryptie ondersteud, zet ook u wachtwoord beveiligd delen uit anders moet elke apparatuur hetzelfde gebruikersaccount hebben. Dan hoort het zoals volgt eruit zien.| ![image](https://user-images.githubusercontent.com/105280571/170566352-acd9b9f7-f3be-439d-ac57-f37292adfb50.png)|

### Bestanden deling toepassen:
Stap |***Uitleg*** | Foto|
---|---|---|
1.| Maak een Folder aan en rechterklik erop ga naar `Toegang verlenen tot` en vervolgens klik op `Specifieke personen` | ![image](https://user-images.githubusercontent.com/105280571/170568469-534bfba8-f181-48d7-a3b4-f3b39ae68580.png) |
2.| Duw op het pijltje en klik op `Iedereen` en duw op `Toevoegen`| ![image](https://user-images.githubusercontent.com/105280571/170569080-88a487d8-71e3-4008-92fe-e37190c4fbb0.png)|
3.| Nu kan je kiezen of de mensen alleen de bestanden mogen `Lezen` of `Lezen en Schrijven` (Als u het op Lezen laat staan kunnen ze niets veranderen of toevoegen in de folder)| ![image](https://user-images.githubusercontent.com/105280571/170570085-d10f5a2e-c9e7-46e2-b858-4ddffeb66eb5.png) |
4.| Duw nu op delen | ![image](https://user-images.githubusercontent.com/105280571/170570998-f899a062-2d3d-403d-9e1c-58fd4dab646e.png)|
5.| Onthoud deze `Path` | ![image](https://user-images.githubusercontent.com/105280571/170571323-d18759a0-5ea7-4425-92f0-25df2fd5c249.png) |

### Bestanden deling gebruik vanaf een andere Computer (Pas dit toe op elke computer waar u het mee wilt delen ook op de uwe)
Stap |***Uitleg*** | Foto|
---|---|---|
1.| Check u ` Network en internet` dat het op `Prive` staat | Zie vorige stappen| 
2.| Open u `verkenner` en ga naar `Computer` en klik vervolgens op `Netwerkverbinding Maken` | ![image](https://user-images.githubusercontent.com/105280571/170573648-48eb60a0-10a5-4add-8c08-1ee7d4606378.png) |
3.| Type vervolgens het `Path` in dat u had onthouden | ![image](https://user-images.githubusercontent.com/105280571/170574027-1acd9f65-33ad-44cd-9341-af1491ae0c4f.png) |
4.| Ga vervolgens terug naar `Deze Pc` |![image](https://user-images.githubusercontent.com/105280571/170574253-7070d6bc-0b91-465b-af29-3523c178287d.png) |
5.| Om het orderlijker te maken rechterklikt u op het bestand en klikt u op `Naam wijzigen` | ![image](https://user-images.githubusercontent.com/105280571/170574444-697627ed-ca9d-4a67-aacd-1b305d28a8e2.png) |

Voila zo kunt u bestanden delen over u thuis netwerk.  

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
