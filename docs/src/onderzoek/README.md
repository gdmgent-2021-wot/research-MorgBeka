---
sidebar: auto

---
# RFID & NFC

> Morgane Bekaert - Web of Things - 3NMD

## UITWERKING
### Verschillende tags

Er zijn heel wat verschillende soorten RFID en NFC tags te verkrijgen. Ik had om te beginnen 3 verschillende soorten meegenomen vanop school. Namelijk een sticker, sleutelhager en een kaart. 

![Sticker](https://arblogography.com/wp-content/uploads/2019/11/CCS-RFID-Sticker-Label-13.56MHz-Frequency-FM1108-SLS.jpg)
![Sleutelhanger](https://www.kiwi-electronics.nl/image/cache/cache/3001-4000/3711/main/9f92-KW-2134-1-0-2-1000x667.jpg)
![Kaart](https://posmea.com/pub/media/catalog/product/cache/c687aa7517cf01e65c009f6943c2b1e9/w/h/whatsapp_image_2020-02-01_at_11.28.15_am.jpeg)

### App - Iphone

Eerst probeerde ik de tags te lezen met verschillende applicaties dat te vinden zijn in de appstore. Ikzelf heb er verschillende uitgetest. 'NFC Tools' & 'NFCScanner' vond ik de beste om de tags te lezen dus heb ik verder gewerkt met deze twee. Ik merkte dat de kaart niet kon gelezen worden met de applicaties maar de sticker & sleutelhanger wel. 

Met de oranje app (NFC Tools) kon ik heel gemakkelijk de tags lezen. Dit kan je doen door de tag tegen de camera te houden aan de achterkant van je iPhone, maar ook als je het tegen de frontcamera houdt werkt het en wordt de tag gelezen.Na het lezen van de tag zie je in deze app heel wat informatie zoals: Tag type, Serial number, Protected by password, memory information, data format, size, writable,... 

Met deze app kan je ook gemakkelijk zaken naar de tag schrijven. Bij het klikken op 'write' krijg je 3 opties te zien: add a record, more options & Write.Om iets nieuw te schrijven klik je op add record, dan krijg je een lijst met verschillende opties zoals bijvoorbeeld text, url, social networks, file, mail, contact, phone number, facetime, location, wifi network, ... 

In mijn voorbeeld gebruikte ik de blauwe sleutelhanger & de url record. Als je deze kiest kanje een url ingeven. Na het toevoegen van de record zie je dat er naast write het aantal bytes van de record komt te staan. Bij de volgende stap klik je op wirte/16bytes. Er komt een popup venster om de NFC-tag opnieuw te scannen. Na het scannen staat de URL op de NFC tag. Dit testte ik nog eens door de tag te lezen. De url kwam tussen alle infogegevens. Wanneer ik op de URL klikte kwam ik terecht op de juiste site. 

Ik wou nog eens testen of de url effectief op de tag staat dus ik opende een tweede app, namelijk NFCScanner. Bij het scannen van dezelfde sleutelhanger kwam de url en kon ik opnieuw naar de site surfen. Ook door gewoon de nfc tag tegen je camera te houden kwam er een popup melding om naar de site te surfen. 


### Reader - Laptop

Na het gebruiken van de verschillende applicatie ben ik beginnen werken met de reader. Hiermee zou je chips moeten kunnen uitlezen en bewerken via de laptop. De lezer dat je hier ziet is een windows reader dus moest aangesloten worden op een windows laptop.

Bij het insteken van de reader installeert hij automatisch nodige software om de reader te laten werken. Nadat als deze software op de laptop stond heb ik nog een andere software geïnstalleerd om de tags te kunnen lezen en of bewerken. Ik installeerde: IDRW V3 T5577 EM4305 Write Read Software.  

Met deze software en een RFID reader zou je bijvoorbeeld de blauwe sleutelhangers moeten kunnen lezen. Op het eerste zicht gebeurde er niet veel bij mij. Bij het klikken op read gebeurde er niets, de software werkte dus nog niet op de laptop dat ik gebruikte. 

Ik ben dan eerst gaan kijken of de reader wel werkte op de laptop. Ik opende notities en scande de kaart. Als ik de kaart boven de reader hield kwam er een pieptoon en verscheen er **Ààà&à&"(&)**. Normaal zou er en id van cijfers moeten opkomen. Het feit dat er bij mijn laptop geen cijfers opkwamen komt doordat mijn mijn laptop een belgisch toetsenbord heeft. Wanneer ik mijn toetsenbord op Nederland zou zetten zou ik volgende code krijgen **0001013515**. 

Online vond ik dat RFID tags niet werken met NFC apparatuur. Het feit dat de kaart werkt met de reader en niet met de NFC apps kan dus verklaren dat het een RFID tag is. Ik kan dus ook besluiten de de sleutelhanger & de sticker NFC tags zijn want deze werken met de NFC apps op mijn gsm en niet met de RFID windows reader. 


Gezien alle software die online stond niet werkte met de lezer, zowel niet voor het lezen, als voor het schrijven. Zijn we opzoek gegaan naar een alternatief. Dit leidde ons naar een Github repo van een gebruiker die alle Windows software had omgezet naar een Python Script om het zo werkend te krijgen. Nu ik er zo op terugkijk hadden we kunnen zien aankomen dat het niet ging werken aangezien de software waarop het gebaseerd was niet functioneerde maar toch. De software herkent de lezer wel maar gaf ons nooit het gewenste respons.

CODE
Eerst wordt de RFID-lezer library ingeladen. Daarna wordt er geprobeerd om de klasse te instantiëren. Indien dit niet lukt gaat men een error printen.
Hierna wordt er beroep gedaan op 2 methodes van de klasse om zo de data van de tag te halen en de ID te printen in de console.
Als laatste zou men ook nog een geluidje afspelen.


### RASPBERRY PI 
Vorige week kregen we dan een NFC-lezer voor de Raspberry PI. Er was maar 1 lezer beschikbaar dus voor het verdere onderzoek heb ik samen gewerkt met Ari. Aangezien de vorige opzoekingen niet werkten, zijn we beginnen zoeken naar documentatie hierover, hopende dat we hiermee wel iets zou kunnen schrijven naar de nfc tags. 

Als eerste hebben we de software van nxp geïnstalleerd op de Raspberry Pi. Bij het installeren kregen we geen errors dus we dachten dat het deze keer wel ging werken. Maar in de terminal bleef er staan “waiting for tag or device…” ook al legden we er verschillende tags op. Deze optie werkte dus helaas ook niet. 

Gezien de meegeleverde software niet werkte zijn we opnieuw aan het kijken naar alternatieven. Zo zijn Ari & ik terecht gekomen op de Github van een zeker Tom. Deze stelde een soort schil rond de originele software beschikbaar. Geschreven in python zodat het gemakkelijk te gebruiken is met een Raspberry, zo zouden we met een script de software kunnen gebruiken. Jammer genoeg hebben we die ook niet werkend gekregen. Het is moeilijk om het precieze probleem te lokaliseren omdat je moeilijk kunt nagaan of de randapparatuur werkt of juist is aangesloten, er is geen lichtje dat brand of geluidje die afspeeld. We kregen ook geen errors te zien in onze terminal, dus zo konden we het probleem ook niet detecteren. 


CODE 
Men begint met 2 libraries in te laden. Uit deze library haalt men een klasse die dan wordt geinstantieerd. 
 
Daarna wordt er gebruik gemaakt van een while om de reader continu te laten lezen.
Hierbinnen gaat men proberen de UID op te halen aan de hand van een methode uit de hierboven ingeladen klasse. Indien dit niet werkt wordt er een error weergeven.



Jammer genoeg hebben we dus niets kunnen schrijven naar de tags. We hebben heel wat verschillende zaken geprobeerd. Vooral bij de laatste mogelijkheden was het moeilijk om te achterhalen waar het probleem zit. We konden niet nagaan of de tags werkten, welke soort tag het was, welke versie,... Bij de raspberry Pi kregen we zoals we daarnet vertelden ook niet veel output, waardoor we niet verder konden onderzoeken waar het probleem precies ligt. 


