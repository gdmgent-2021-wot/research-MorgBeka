---
sidebar: auto

---
# RFID & NFC

> Morgane Bekaert - Web of Things - 3NMD

## RFID

### Wat?

RFID = **Radio-frequency identification.**

Dit is een technologie om van op een afstand informatie op te slaan en af te lezen van tags, die RFID-tags zitten op of in objecten of levende wezens. Bijvoorbeeld in chipkaarten die gebruikmaken van NFC.

Deze technologie maakt gebruik van radiogolven om informatie draadloos op afstand te lezen of te versturen. Deze informatie wordt gelezen door een RFID-reader en daarna verwerkt door intelligente software

NFC is de afkorting voor Near Field Communication. Dit is een vorm van RFID. Bij RFID draait het vooral om opslag & verzenden van informatie in 1 richting. Terwijl 
NFC communiceert in 2 richtingen en kan het ontvangen signaal ook zelf verwerken. 
NFC is een techniek die onder andere toegepast in gsm’s als betaalmiddel of in ticketsystemen. 

![Toepassing RFID](https://i.pinimg.com/originals/d5/70/c1/d570c1a132ef3ea1c456fa9f4bfd57c7.jpg)

### Geschiedenis 




### Voordelen & nadelen RFID

RFID heeft heel wat **voordelen** zoals
- Geen fysiek contact nodig om te scannen 
- Geen zichtlijn nodig zoals bv bij de streepjescode
- Veel grotere afstanden mogelijk dan bij streepjescode
- Honderden codes kunnen in een of enkele seconden worden gelezen
- Unieke codering maakt het mogelijk om productvervalsing te bemoeilijken en/of snel op te sporen
- In tegenstelling tot streepjescodes blijven RFID tags leesbaar bij weersinvloeden, vuil, … enz
- Vervalsen van RFID-tags is veel moeilijker dan bij de streepjescode 

Zoals bij alles zijn er natuurlijk ook enkele **nadelen**

- Privacy kan in gevaar komen 
- Als identificatiedocumenten zoals bijv paspoort een tag hebben kan men hier misbruik van maken door mensen te volgen
- RFID kan medische apparatuur op afstand verstoren 
- Tags kunnen (geringe) elektromagnetische straling veroorzaken 
- Lees/schrijfmogelijkheden van de RFID-tag kunnen het mogelijk maken dat er ongemerkt fraude wordt gepleegd;


### Soorten 

Er bestaan heel wat verschillende RFID-tags in uiteenlopende vormen en afmetingen. Het kan zijn dat ze alleen kunnen lezen of zowel kunnen lezen en schrijven.

RFID-tags kunnen actief of passief zijn.

#### Een passieve tag 

Een passieve tag heeft geen eigen energiebron, hij gebruikt ontvangen signalen om zichzelf te activeren (de energie wordt bevoorraad door de tag lezer).

Ze benutten het elektromagnetisch veld van een rader om een stroom te induceren in een spoel, waarmee dan de chip gevoed wordt. 

Deze tags kunnen op verschillende manieren gebruikt worden. bijvoorbeeld tussen een kleeflaag en een papier label → zo worden slimme RFID-labels gemaakt

Maar ze kunnen ook geïntegreerd worden in apparaten of verpakkingen.

##### Voordelen
- Niet duur om te maken 
- Heel klein 
- Gemakkelijker om te produceren dan actieve tag 

##### Nadelen
- Niet over een grote afstand (enkele cm tot ong 5m) 
- Blijven lang leesbaar (zelfs wanneer ze niet meer vasthangen ah voorwerp of al verkocht zijn & dus niet meer getraceerd moeten worden 
- Te klein om sensoren in te plaatsen die werken op elektriciteit 

![A roll of Passive RFID inlays](https://www.atlasrfidstore.com/product_images/uploaded_images/active-rfid-vs-passive-rfid-2.jpg)

#### Een actieve tag 

De actieve tag bevat  een eigen zender en stroombron, meestal is dit een batterij of zonnecel.
De tag kan worden gelezen en geschreven met de reader, deze ontvangt en zendt met een antenne  (deze wordt ook gateway genoemd) radiogolven.
Ze hebben de mogelijkheid om de real-time locatie van de tag bij te houden


##### Voordelen
- Ze kunnen een signaal over een grote afstand uitzenden (van 100m tot enkele km)   
- Sensoren kunnen meteen gebruik maken van de elektriciteit 

##### Nadelen
- Duurder dan passieve tag
- Kan niet zonder batterij 
- Groter

![Example of an extremely rugged active RFID tag](https://www.atlasrfidstore.com/product_images/uploaded_images/active-rfid-vs-passive-rfid-3.png)


#### Links een passieve tag en rechts een actieve tag 
![Passive&Active tag](https://www.researchgate.net/publication/269725122/figure/fig2/AS:668966766792712@1536505514345/RFID-tags-Passive-left-and-active-right-Source-authors-elaboration.png)



### Enkele toepassingen 

- **Diefstalpreventie**
  
  - Bijvoorbeeld bepaalde kartonnen dozen met dure drank (whisky)  bevatten RFID-tags waardoor deze beveiligd zijn tegen diefstal 
  - Door middel van RFID kan een kledingstuk van fabrikant tot kassa worden getraceerd 
  
- **Personen- en dierenidentificatie**
  
  - De mogelijkheid bestaat om een tag in een mens/dier te plaatsen. Deze tag kan dan bijvoorbeeld informatie bevatten over identiteit of rijbewijs
  
    - huisdieren kunnen door dierenarts worden voorzien van een identificatiechip
    - In Rotterdam is er een beachclub waar er iets dergelijks in de arm geplaatst wordt. Klanten kunnen hier geld opladen en daarmee dan betalen wanneer ze iets bestellen 
    - Resorts → polsbandjes voor gasten die gekoppeld worden aan kamer, restaurant, bar (arrangement-identificatie)  
    - Zwembaden → siliconen polsbandjes met een chip erin voor onder andere toegang en kluisje 

![Chiplezer voor het uitlezen van RFID chips bij dieren](https://media.agrishop.nl/nl/article-images/shop800px/82019-voss-pet-chipreader-rfid-reader-rt250-2.jpg)

![Tag in hand](https://www.diamandis.com/hubfs/Diamandis_March_2017-Theme/Images/tumblr_inline_nfk2fgmG5M1sjf6lz.jpg)




- **Bankbiljetten**
  
  - Tegen vervalsing

- **Merkproducten** 
  
  - Tegen vervalsing bijvoorbeeld designerkleren 

![Kledij](https://rfidresearchers.files.wordpress.com/2010/12/images.jpg?w=584)

![Kledij](https://cdn.frankwatching.com/app/uploads/2011/04/RFID-chip2-266x200.jpg)

- Paspoort & andere ID-bewijzen zoals studentenkaart 
  
![Tijdregistratie](https://i.pinimg.com/564x/18/6a/92/186a92e196ef3709a580943a1ae3cd0a.jpg)

- Tijdwaarneming bij sportwedstrijden 
 
![Tijdregistratie](https://www.jahoma.nl/timereg/wp-content/uploads/Jahoma-ChipTiming-SchermSnapShot-Deelnemerfoto-controle-details-700x630.jpg)

- …



## NFC

### Wat?

NFC = **Near Field Communication.** 

Dit is een vorm van RFID. Bij RFID draait het vooral om opslag & verzenden van informatie in 1 richting. Terwijl 
NFC communiceert in 2 richtingen en kan het ontvangen signaal ook zelf verwerken. 
NFC is een techniek die onder andere toegepast in gsm’s als betaalmiddel of in ticketsystemen. 

![Toepassing NFC](https://images.samsung.com/is/image/samsung/p5/nl/discover/travel/wat-is-nfc-en-waarom-zit-het-op-mijn-mobiel/nfc-wat-is-nfc-hero.jpg?$ORIGIN_JPG$)

<!-- ::: tip
**Wat is het verschil?**

loremipsumhakjrlefqn;sdfnqsdnfjkjzhr

::: -->
