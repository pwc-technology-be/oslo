**Informatie Vlaanderen**

Werkgroep OSLO² en "Meld Een Fout"

Datum: 28/03/2017 -- 13:00 -- 14:30

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Goedele Van der Spiegel, Carolien Willen, Jurgen Dooms,
Michiel De Keyzer, Jens Scheerlinck

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Actielijst](https://drive.google.com/open?id=1ol-KHZSkwmiwZVU166074YOj5XfojHUkbSx-Hi0DgPg)

-   [Mapping](https://drive.google.com/open?id=1SJSe_JdWHia7XcipoWRwyVtfolZ7Vt-9futzR59Uobw)

-   [UML datamodel](https://drive.google.com/open?id=0B3DdQTFc4B-VRzQ5czNUQlA2QzA)

-   [JSON-LD voorbeelden](https://drive.google.com/open?id=0B3DdQTFc4B-VZlZad0F5RUlZM0E)

-   [Website voor JSON-LD visualisatie](http://json-ld.org/playground/)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Het doel van dit werkgroepoverleg bestond erin de laatste versie van het
voorgesteld model te bespreken, het toelichten van enkele uitgewerkte
voorbeelden op basis van de use cases en het afronden van de laatste
open actiepunten.

Agendapunten:

1.  Overlopen van de actielijst en de daaruit voortvloeiende wijzigingen aan het model;

2.  Bespreken van de voorbeelden die de use cases afdekken;

3.  Vastleggen van vervolgacties om deze oefening te landen.

Verloop
=======

-   De wijzigingen aan het model werden voorgesteld door Michiel en Jens:

    -   De "indiener" klasse werd vervangen door een generieke "participatie" relatie tussen een melding en een "Agent". Aan deze participatie-relatie kan een rol worden toegewezen, deze rollen werden op basis van discussie vastgelegd als een enumeratie met rollen: indiener, validator en behandelaar. De rol van "meldingsorganisatie" werd verplaatst als attribuut onder de klasse "Melding", omdat deze meldingsorganisatie een betekenis heeft doorheen de hele levensloop van de melding en niet zozeer een rol speelt in de afhandeling (GTMF3 in actielijst).

    -   Generieke objecten kunnen gelinkt worden aan een melding, deze kunnen een identificator, tekstuele omschrijving en extra informatie (bijlage, URL,\...) bevatten. Specifieke types van een object zijn geometrie en een observatie (refereert naar een dataveld, in het kader van een terugmelding). Voor deze subtypes geldt géén wederzijdse uitsluiting. Een object kan zowel een geometrie als een observatie zijn op hetzelfde moment, door de attributen van beide subtypes te gebruiken (GTMF4 en GTMF11 in actielijst).

        -   De vraag wordt gesteld of in gevallen waar geometrie en observatie samenvallen, er nood is aan een afzonderlijke identificator voor de geometrie. Dit moet verder worden onderzocht door het model af te toetsen aan praktijkvoorbeelden van de bestaande GRB en CRAB meldingssystemen.

    -   Het concept "Collection" werd geïntroduceerd, dit is een verzameling van objecten waar een eigen identifier kan aan gekoppeld worden. Verder bezit de collectie geen eigen attributen. Hierdoor kunnen clusters van objecten bij elkaar gehouden worden, bv. om de use case te ondersteunen waar behandelaar van meldingen bepaalde filters op applicatie niveau willen bewaren voor hergebruik bij het opnieuw inloggen (GTMF5 en GTMF15 in actielijst).

    -   Om applicaties die zich aansluiten op de GTMF de mogelijkheid te bieden terugmeldingen te ontvangen is het noodzakelijk dat zij bij wijze van configuratie kunnen bepalen welke concepten en attributen bestaan binnen hun dataset waarop een terugmelding kan worden gedaan. Om dit te bewerkstelligen werden op basis van de [Data Cube Vocabulary](https://www.w3.org/TR/vocab-data-cube/) een aantal extra klassen toegevoegd aan het model om een generieke datastructuur te definiëren. Dit zal toelaten om een observatie in het model (terugmelding) te linken aan het informatiemodel in het achterliggende bronsysteem (GTM13 in actielijst).

    -   Op aangeven van Raf Buyle werd het [Open311](http://www.open311.org/) initiatief voor meldingen door gebruikers aan overheden bestudeerd. Uit de analyse bleek (GTMF14):

        -   Open 311 is een initiatief dat focust op location-based issue-tracking

        -   Het is niet zozeer een vocabularium dat wordt vastgelegd maar eerder een API specificatie. Binnen die API specificatie worden ook een aantal attributen voor een melding vastgelegd.

        -   311 is geschikt voor initiatieven zoals \'Fix My Street\' maar kan momenteel niet worden toegepast voor terugmeldingen (op data).

        -   Wat zeker wél interessant kan zijn is de manier waarop zij melders verwittigen wanneer iets is opgelost aan de hand van notificaties. Dit zal bekeken worden in het kader van het datamodel voor Melding (wat eveneens reeds opgestart is).

    -   Om een meer fijnmazige notificatie naar de gebruiker toe te laten over de status van de melding, vooral wanneer een melding betrekking heeft op vele objecten (of observaties), zal een link voorzien worden tussen de klassen "Status" en "Object". De relatie heeft als doel informatie te capteren van de afhandeling van de melding die op een specifiek object betrekking heeft, en niet wat de status is van het object zelf.

    -   Tot slot werd besproken om contact op te nemen met de collega's in Nederland die met een gelijkaardig project rond (terug)meldingen bezig zijn.

Besluit en acties
=================

1.  Mits het doorvoeren van de besproken wijzigingen kan het model afgeklopt worden als finaal. Er wordt bijgevolg voorlopig geen nieuw werkgroepoverleg ingepland.

2.  PwC zal het model verder toetsen op basis van voorbeelden van de GRB en CRAB meldingssystemen (deadline 14/04/2017).

3.  Goedele en Carolien voorzien in een extra use case met betrekking tot de LED databank. PwC werkt op basis hiervan ook een voorbeeld JSON-LD uit (deadline 19/04/2017).

4.  PwC voorziet in Nederlandstalige vertalingen van de labels en definities van hergebruikte internationale vocabularia (deadline 14/04/2017).

5.  PwC plant een meeting in met de collega's uit Nederland voor een overleg waarbij we onze aanpak op elkaar afstemmen (deadline 14/04/2017).

6.  De werkgroep zal vervolgens de mapping valideren alvorens PwC de relevante documentatie en technische specificaties kan genereren (deadline 19/04/2017).
