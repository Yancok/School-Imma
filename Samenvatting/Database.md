# Database
> Dit zijn de commands voor SQLite3.  
Om een `...>` weg te doen doe je `CRTL+C`  

## Basics
![image](https://user-images.githubusercontent.com/105280571/172013730-b836c74c-f8d0-482d-9eff-efb2ca04a24d.png)  
**Blauw** is een *Rij* en **Rood** is een *Tabel*.  

## Dot-commands

Command | Uitleg |
---|---|
.open `Path`| Opent een database|
.read `Path`| Past een voorgemaakte Query toe |
.help `...`| Geeft u advies over wat je erna schrijft |
.quit| Je sluit u SQLite3 af. |
.schema `Path`| Geeft u het hele schema van de database|
.tables | Weergeeft je alle huidige tabellen weer |

### Modes
Handige Modes | Uitvoering |
---|---|
.mode `Table` | ![image](https://user-images.githubusercontent.com/105280571/171162511-2602287e-ab25-4079-8527-708c25fecf70.png)|
.mode `box` | ![image](https://user-images.githubusercontent.com/105280571/171162891-c4a1e274-0ddc-4a8d-b041-eb8623406294.png) |
.mode `column`| ![image](https://user-images.githubusercontent.com/105280571/171162986-25331024-974f-4215-8b7f-7f95a0ae1639.png) | 
> Er zijn meer modes als je die wilt zien doe je `.help .mode`  

## SQLite Commands
Command | Uitleg |
----|---|
SELECT `rijen` | Weergeeft de rijen die je wilt laten zien van de database |
`Rijen` AS `naam` | Je geef de tabel een nieuwe naam in de Query |
FROM `tabel` | Laat de tabel zien |
INSERT INTO (`Rijen`) VALUES (`Inhoud`) | Zo voeg je rijen aan de tabel toe met inhoud |
WHERE| Als je een voorwaarde wilt doen|
JOIN `tabel` (ON `Tabel.Rij = Tabel.Rij`)| Voegt een tabel toe (ON verbindt een PK met FK zodat er geen overbodige gegevens zijn.) | 
ORDER BY (ASC/DESC) | sorteert op Oplopend (ASC) of Aflopend (DESC) |
LIMIT `Aantal` (OFFSET) | LIMIT laat er maar het aantal zien (OFFSET zorgt bepaald je op welke rij het start) |
LIKE| Een vervanging van `=` bv voor strings | 
DROP TABLE `tabel`| Verwijdert tabel |
DROP TABLE IF EXISTS`tabel` | Verwijdert tabel als hij bestaat |


## Jokers
Jokers | Uitleg |
---|---|
% |  |
![image](https://user-images.githubusercontent.com/105280571/171999579-de3e5bf8-9168-4828-95a4-c67efe507b58.png) | Twee strings samen plakken |

## Aggregatie-functie
Aggregatie | Uitleg |
---|---|
COUNT(` `) |  Telt de rijen op en geeft een interger |

## Powershell commands
Command | Uitleg |
----|---|
cd \ | Je gaat naar u root folder |
Get-Content `bestand` | Krijg je de inhoud van het tekstbestan |
Format-Hex `bestand` | dit toont de bytes van het bestand
dir | Je ziet wat er allemaal in u PATH zit |
mkdir `naam` | Je maakt een nieuwe folder aan met de naam |
cd `path` | Je gaat naar het Specifieke Path |
sqlite3 | Je opent SQLite3 |
git clone `link` | Download de link in u PATH |


## Theorie
Sommige arugementen hebben een `-` of `--` dit noemen we vlaggen.  
`code .` doen in een CMD open je u PATH  in visual studios.  
