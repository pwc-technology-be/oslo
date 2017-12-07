**Informatie Vlaanderen**

Overleg gebruik INSZ versus Eigen Sleutel

Datum: 08/03/2017 -- 15:30 -- 16:30

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Goedele Van der Spiegel, Bart Misseeuw, Dirk Gepts, Valère
Bouserie, David Van den Brande, Michiel De Keyzer, Jens Scheerlinck

Verontschuldigd: An Boes, Bruno Devrieze, Katrien Mostaert

Verslaggever: Jens Scheerlinck

Bijlage(n):
[presentatie](https://drive.google.com/open?id=1jbnp7uG74XCcuUd45xhCauCw6SJ8S1yMkj2OMNKdBoI),
[informatie m.b.t. mogelijke oorzaken voor wijziging
INSZ](https://drive.google.com/open?id=0B3DdQTFc4B-VYi1uMDFSTDd5YkU)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Er bestaan verschillende initiatieven (zowel bestaand als in uitvoering)
rond het uniek identificeren van een persoon. Vanuit Burgerloket is er
een architecturale vraag ontstaan met betrekking tot het uniek
identificeren van een persoon. De opzet van deze vergadering is het
uitwisselen van gegevens met betrekking tot de verschillende
initiatieven en mogelijkheden om in een later stadium een gefundeerde
beslissing hieromtrent te kunnen nemen.

Verloop
=======

1.  Noden vanuit Burgerloket:

    a.  Persoon uniek identificeren en koppelingen maken overheen verschillende bronnen.

    b.  Burgerloket is een lopend project, het is noodzakelijk om gebruik te maken van een bestaand initiatief dat meteen in de praktijk inzetbaar is.

2.  Use cases voor een unieke en persistente identificator voor personen:

    a.  Opvolgen van lopende zaken voor en na een geslachtswijziging

    b.  Raadplegen van attesten na verhuis van BIS register naar Rijksregister

    c.  Bewaren van relaties met andere personen (bv. referentiepersoon)

    d.  Tonen van historiek persoonsgegevens in Burgerloket (na wijziging INSZ)

    e.  Nood om een minder privacy gevoelige sleutel te hebben voor het aanbieden van meer functionaliteiten zonder in aanraking te komen met het INSZ, wat extra machtigingen vereist.

3.  Bestaande sleutels en initiatieven:

    a.  INSZ

      -   INSZ bestaat uit rijksregisternummers en BIS-nummers.

      -   In het kader van lopende zaken ontvangen afleverende overheden wijzigingen (mutaties) van het rijksregister. In de bronsystemen moet het oude INSZ nummer vervangen worden door het nieuwe.

      -   De link van het oude naar het nieuwe INSZ wordt bijgehouden. Zowel het rijksregister (wekelijks) als de kruispuntbank voor sociale zekerheid (dagelijks) stuurt naar MAGDA een bestand met mutaties. Alle applicaties die gebruik maken van het INSZ zijn verplicht deze mutaties te verwerken in hun systemen.

      -   Authentieke bronnen vangen deze problematiek reeds op.

      -   Voor nieuwe applicaties: noodzakelijk om functionaliteit te implementeren om mutaties te verwerken.

      -   In MAGDA: bij opvragen van het oude INSZ nummer wordt in de response het nieuwe meegegeven.

      -   Daarnaast is er ook de privacygevoeligheid in verband met het INSZ, dit kan het topic zijn van een aparte meeting.

      -   Gebruik van INSZ vereist een machtiging + het geëncrypteerd stockeren in de database, indien dit niet een interne database is van de Overheid.

      -   Valère heeft een document gedeeld waarin alle redenen opgelijst staan waardoor een INSZ nummer van een persoon kan wijzigen:

          -   Het dossier wordt gecreëerd terwijl de persoon niet voldoet aan de inschrijvingsvoorwaarden

          -   Fout in de geboortedatum of betreffende het geslacht bij de verzameling

          -   Er bestaan twee identificatienummers voor dezelfde persoon

          -   Verzameling van meerdere dossiers per vergissing (programmafout)

          -   Geslachtsverandering

          -   Incorrecte Identiteit

      -   Kruispuntbank voor sociale zekerheid biedt nu nu een service aan waarbij een INSZ nummer kan verstuurd worden en in de response zit de volledige historiek (zowel naar het verleden als de toekomst toe).

    b.  Vlaamse sleutel

      -   Op dit moment is hier geen extra informatie over gekend door de aanwezigen. Actiepunt wordt meegenomen om hier meer informatie over te vergaren via Bruno Devrieze.

    c.  "vo\_idv" sleutel IDM

      -   Wordt gebruikt binnen ACM IDM.

      -   Aangemaakt in het kader van Web IDM toepassingen.

      -   In het leven geroepen om use case te dekken waarbij in communicatie (bv. met eerste lijn of tweede lijn support) een persoon uniek kan geïdentificeerd worden zonder het INSZ nummer te gebruiken, wat niet zomaar mag ontsloten worden omwille van privacy wetgeving.

      -   De meeste toepassingen krijgen echter ook het INSZ nummer binnen.

      -   Eens de gebruiker aangemaakt is binnen Web IDM wordt aan alle gebruikers enkel de vo\_idv sleutel getoond. De link met INSZ wordt wel opgeslagen maar wordt in praktijk niet gebruikt voor vertaal doeleinden, behalve wanneer mensen rechtstreeks inloggen via hun eID. Omgekeerd, de vertaling van een vo\_idv sleutel naar het INSZ, komt niet voor.

      -   Er wordt een nieuwe vo\_idv sleutel aangemaakt wanneer iemand met een nieuw INSZ nummer. Mutaties worden dus niet opgevangen en toegekende rechten worden niet automatisch overgezet.

      -   Een applicatie kan in zijn integratiedossier bij ACM IDM aangeven welke informatie ze wil krijgen over een bepaald persoon. Voor burgers zijn de volgende velden beschikbaar: INSZ, voornaam en familienaam. Deze informatie komt echter niet rechtstreeks uit IDM.

      -   De vo\_idv sleutel wordt wel ontsloten buiten de ACM IDM wereld voor technische communicatie met andere applicaties. Indien een applicatie niet gemachtigd is om het INSZ te gebruiken kan de vo\_idv sleutel gebruikt worden om een persoon uniek te identificeren en na te gaan welke rechten deze persoon heeft voor een specifieke applicatie.

      -   Probleem: partners die niet via ACM IDM zijn aangesloten maar enkel via FAS (CSAM) kunnen geen gebruik maken van de vo\_idv sleutel.

      -   Meer informatie over de machtigingen die ACM IDM heeft kan verkregen worden bij Pieter Leenaerts of Stefanie Kerkhofs.

      -   David Van den Brande geeft ter informatie mee dat er reeds een meeting met Stefanie Kerkhofs is ingepland om te bekijken of ACM IDM een rol kan spelen in het verhaal van het Burgerloket Profiel.

    d.  FOD Fin unieke sleutel

      -   Werd een tiental jaar geleden aangemaakt om bij een wijziging van het INSZ de historiek bij te houden van een persoon en zijn dossiers/aangiftes bij FOD Fin.

      -   Geïmplementeerd als centraal systeem dat uitsluitend communiceert met applicaties van FOD Fin (interne keuken). Alle FOD Fin applicaties gebruiken de unieke FOD Fin sleutel en de vertaling wordt beheerd door dit centraal systeem. Deze sleutel wordt niet ontsloten naar andere applicaties buiten FOD Fin.

      -   Deze aanpak heeft ook een belangrijk nadeel: alle applicaties die uniek nummer nodig hebben moeten connecteren op systeem dat uniek nummer beheert. Zorgt voor zware belastingen op het vertaalsysteem wat de performantie niet ten goede komt.

Besluit en acties
=================

1. Bruno Devrieze geeft input in verband met de status van de 'Vlaamse sleutel'. **-\>** **Input Bruno 09/03**: *Is allesbehalve vlaamse sleutel: is nummer dat ze gebruiken bij O&V. Gert weet daar niks van (en ik denk niemand anders dan ik, mss Valere)*

2. Momenteel lijken de enige valabele mogelijkheden voor gebruik binnen Burgerloket het INSZ nummer (sterke authenticatie) en de vo\_idv sleutel (zwakke of zwak+ authenticatie). vo\_idv lijkt dan vooral relevant voor in tweede fase van het Burgerloket.

3. Voor lopende zaken: verantwoordelijkheid moet expliciet bij de bronnen gelegd worden om INSZ mutaties te verwerken in bronsystemen en deze dan door te geven aan DOSIS/Burgerloket.
