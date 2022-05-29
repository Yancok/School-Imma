# Basis Programmeren
### Leer vooral de ***Object Browser*** te gebruiken das FREE CHEAT 
Maar onthoud hoe je moet `Declareren` dat moet je uit u hoofd kennen.  
![image](https://user-images.githubusercontent.com/105280571/170672788-cfeba0c4-83f9-461f-937a-f8562addfc6d.png)

> Als het tussen `[ ]` staat dan is het uitleg wat er moet staan.

## Operatoren
> Dit moet je wel ***leren*** uit u hoofd

*Operatoren* | *Uitleg* |
---|---|
`<`  | Kleiner dan |
`<=` | Kleiner dan of gelijk aan |
`>`  | Groter dan |
`>=` | Grotder dan of gelijk aan |
`==` | Gelijk aan |
`!=` | Niet gelijk aan |
`&&` | AND-poort of alle twee voorwaarden moet True zijn |
![image](https://user-images.githubusercontent.com/105280571/170676464-99aa02f1-b34e-4185-911d-a2698a6c1bc1.png) | OR-poort of 1 van de 2 voorwaarden moet True zijn |
`++` | Verhoogt het Getal met 1 |
`--` | Verlaagt het Getal met 1 |
`+=` | Verhoogt het Getal met wat achter de = staat |
`-=` | Verlaagt het Getal met wat achter de = staat |

## String Methodes  
> Het woord: `Voorbeeld` staat in strVoorbeeld.  
> > *OP HET EXAMEN KAN JE DIT ALLEMAAL TERUG VINDEN BIJ* ***OBJECT BROWSER*** en tik je in `System.String` of `String`  
> Daar staat ook de uitleg in hoe je het toepast.


*Ingebouwde Methode* | *Uitvoer/Aanpassing*| *Uitleg* |
---|---|---|
strVoorbeeld`.ToUpper()`| VOORBEELD | Zet heel de String in druk letters.|
strVoorbeeld`.ToLower()`| voorbeeld | Zet heel de String in kleine letters.|
strVoorbeeld`.Substring([start index],[lengte])` | oor | Neemt maar een aantal letters uit de string |
strVoorbeeld`.Length` | 9 | Geeft het aantal letters van de String in Int | 
strVoorbeeld`.Trim()` | Voorbeeld | Verwijdert de Spaties voor- en achter de string |


## Interger Methodes  
> Het getal: 10 staat in intGetal  
> > *OP HET EXAMEN KAN JE DIT ALLEMAAL TERUG VINDEN BIJ* ***OBJECT BROWSER*** en tik je in `System.Math` of `Math`  
> Daar staat ook de uitleg in hoe je het toepast.

*Ingebouwde Methode* | *Uitvoer/Aanpassing*| *Uitleg* |
---|---|---|
`Math.Pow(intGetal,[De macht])`| 100 | Doet verhoogt het getal met de macht hier dus 10^2.|
`Math.Round(intGetal,[Deciamelen])`| 10.00 | Rond het getal af tot het gegeven decimalen. |
`Math.PI`| 3.14 | Dit geeft PI |

## DateTime methodes
> Declareren van DateTime gebeur als volgt: `DateTime dteDatum = new DateTime([intJaar],[intMaand],[intDag])`  
> > *OP HET EXAMEN KAN JE DIT ALLEMAAL TERUG VINDEN BIJ* ***OBJECT BROWSER*** en tik je in `System.DateTime` of `DateTime`  
> Daar staat ook de uitleg in hoe je het toepast.


*Ingebouwde Methode* | *Uitvoer/Aanpassing*| *Uitleg* |
---|---|---|
`DateTime.Today` | 27 mei 2022 | Geeft de datum van de computer. |
`DateTime.Days` | 27 | Geeft het aantal dagen weer. (na een uitvoering bv.) |
`DateTime.AddDays([Het aantal dagen])` | 30 | Voegt dagen toe aan u orginele datum.|

## Random Methodes
> Declaratie: `Random rndGetal = new Random()`
> > *OP HET EXAMEN KAN JE DIT ALLEMAAL TERUG VINDEN BIJ* ***OBJECT BROWSER*** en tik je in `System.Random` of `Random`  
> Daar staat ook de uitleg in hoe je het toepast.

*Ingebouwde Methode* | *Uitvoer/Aanpassing*| *Uitleg* |
---|---|---|
intGetal = rndGetal`.Next([Min],[Max])` | 1 of 2 of ... of 9 | Geeft een getal tussen de Min en Max |
dblGetal = rndGetal`.NextDouble()` | 0,0 | Geef een random Komma getal |

## Array Methodes
> Declaratie: `int[] arrGetallen = new int[10]`   
> Dit maakt een Array van 10 lang dus van 0 tot en met 9.
> > *OP HET EXAMEN KAN JE DIT ALLEMAAL TERUG VINDEN BIJ* ***OBJECT BROWSER*** en tik je in `System.Array` of `Array`  
> Daar staat ook de uitleg in hoe je het toepast.

Belangerijke code| Uitleg|
---|---|
![image](https://user-images.githubusercontent.com/105280571/170677612-c09949ce-4789-40f5-bfc3-a8a8d9bef932.png)| Zo ga je heel u Array af.|
![image](https://user-images.githubusercontent.com/105280571/170678321-e6c2ced2-908c-4fa2-aab3-1fd0fd4ddd9f.png) | 2 Dimensioneel Array. |

*Ingebouwde Methode* | *Uitleg* |
---|---|
`Array.Sort(arrGetallen)` | Sorteerd de Array |
`Array.Reverse(arrGetallen)` | Keert de Array om |


## List Methodes
> Declaratie: `List<int> lstGetallen = new List<int>()`   
> Dit maakt een Array van 10 lang dus van 0 tot en met 9.
> > *OP HET EXAMEN KAN JE DIT ALLEMAAL TERUG VINDEN BIJ* ***OBJECT BROWSER*** en tik je in `System.List` of `List`  
> Daar staat ook de uitleg in hoe je het toepast.

Belangerijke code| Uitleg|
---|---|
![image](https://user-images.githubusercontent.com/105280571/170707702-be708e16-be0c-403a-b733-5dd5977126ce.png)| Moet je schrijven anders gaat list niet werken.|


*Ingebouwde Methode* | *Uitleg* |
---|---|
lstGetallen`.Add("Voorbeeld")` | Sorteerd de List |
lstGetallen`.Insert([index],"Voorbeeld")` | Keert de List om |
lstGetallen`.Count` | Telt aantal elementen in de lijst |
lstGetallen`.Clear()` | Maakt de lijst leeg |
lstGetallen`.RemoveAt([index])` | Verwijdert het element op de index plaats |
lstGetallen`.Remove("Voorbeeld")` | Verwijdert het Eerst voorkomende "Voorbeeld" |
___
# OOP
OOP - Object oriented Programming

Objecten: Console, Form, button, ... worden beschreven in een Klasse.  
![image](https://user-images.githubusercontent.com/105280571/170867922-720d60b2-c00c-4f96-bd50-882f72e3c2b5.png)  
**Klassen** gebruiken vwe om *Objecten* te beschrijven.  
*Klassen* die bij elkaar horen, groeperen we in een **Namespace**.  

Het *LagenModel* bestaat uit twee Lagen, de Presentation Layer en de Business Layer en wij programmeren in de **Business Layer**.  

De werkmanieren:  
* TOP-DOWN
  * Goed voor kleine programma's
  * Code is bijna niet flexibel en zelden *herbuikbaar*
* BOTTOM-UP
  * Zoeken naar objecten
  * Klassen schrijven
  * Geschikt voor *complexe* programma's en *hergebruik*
 
 **Members** van de Klasse | *Uitleg* |*Voorbeeld* | *Overerven* | 
---|---|---|---|
Velden | Zijn geheugen plaatsen | Naam, Achternaam | Nee |
Eigenschappen| Lezen/Schrijven van Data | Lengte, Leeftijd, Vachtkleur | Ja |
Methodes | Bewerkingen uitvoeren | Functies, Procdures | Ja |
Functies | `Methodes` met een ***Return*** waarde | Lopen, Blaffen | Ja |
Procedures | `Methodes` **Zonder** Return waarde | / | Ja |
Constructors | Code die wordt uitgevoerd bij het aanmaken van een object  | / | Nee |

**inklapseling** zijn enkel gekend in de klasse vna het object (Private)  
Voordelen van inkapseling:
+ Beter controle op toegankelijkheid van data  
+ Code vaan een klasse kan aangepast worden zonder andere code te beinvloeden   

**Eigenschappen** worden meestal `Public` gedeclareerd zodat ze toeganklijk zijn vanuit andere klassen.

*Naam* van een property heeft `2 regels`:
1. Geen _
2. Eerste letter Hoofdletter
> Dus een voorbeeld: Voorbeeld  

**Zeer handige foto**  
![image](https://user-images.githubusercontent.com/105280571/170868641-d9b419d4-01ef-44de-bdde-8d17ee7fde09.png)


Onder *objecten* kunnen verschillende vormen aannemen:  
* **Tastbaar**: Hond,auto, persoon   
* **Abstact**: Een ding of concept    
* **Interactie**: Een aankoop  
* **Een rol**: student, beheerder  

___
# Blokschema's
