**Informatie Vlaanderen**

Werkgroep Informatiemodel Notificatiecomponent

Datum: 05/07/2017 -- 12:30 -- 13:30

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Bart Misseeuw, Goedele Van der Spiegel, Niko Tanghe, Dries
Beheydt, Michiel De Keyzer, Jens Scheerlinck

Verontschuldigd: David Van Den Brande, Raf Lauriks

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Nieuwe versie van het UML model op basis van de ontvangen feedback](https://drive.google.com/open?id=0B3DdQTFc4B-VQTM4NnJFZUdVQkE)

-   [Up-to-date versie van de actielijst](https://drive.google.com/open?id=1muvFEysP6UNGWGoe2BkoL7aqiUAZk5QwOa4vaElpsqs)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

-   Bespreken van de feedback ontvangen van ontwikkelaars (Niko) en vanuit architectuur invalshoek.

-   Afkloppen van updated model en sluiten van resterende open actiepunten.

Verloop
=======

Overlopen van open items in de actielijst:

-   N1: concept "Inbox"

    -   Inbox weglaten uit informatiemodel voor Notificatiecomponent.

    -   Zal wel in het OSLO² model gedefinieerd blijven, op die manier kan het ook in de toekomst eventueel terug worden opgenomen als er specifieke use cases voor zijn (bv. notificaties die niet gelinkt zijn aan een INSZ of ondernemingsnummer).

    -   Om meerdere "lezers" in één onderneming (bv. zaakvoerder, secretaresse,\...) notificaties te laten ontvangen zonder deze personen te moeten identificeren a.d.h.v. hun INSZ, zal als bestemmeling voor het Notificatiebericht "Organisatie" genomen worden. Organisatie heeft contactinfo met één of meerdere e-mailadressen en wordt geïdentificeerd door een ondernemingsnummer.

    -   In het profiel voor ondernemers (ondernemerloket) dient er een mapping te gebeuren tussen type notificatie en de e-mailadressen die deze notificatieberichten mogen ontvangen.

    -   Voor wat betreft passieve kanalen, zal er géén onderscheid gemaakt kunnen worden naar wie een notificatiebericht te zien krijgt. Dat zal iedereen zijn die aanmeld in naam van de onderneming.

-   N3: notificatie voorkeuren, thema mee opnemen?

    -   Thema voorkeuren worden volledig buiten scope gelaten.

-   N4: meegeven van Google Markup en template velden

    -   Alle key-value pairs zitten verzameld in het attribuut "hasBody" van Notificatiebericht.

    -   Enkele voorstellen zullen uitgewerkt worden door PwC naar alternatieve benamingen voor dit veld. **\[UPDATE\]** in updated model hebben we gekozen voor "inhoud" als naam voor de eigenschap en "SleutelWaardePaar" voor het datatype (een term die door IBM in hun documentatie wordt gehanteerd).

    -   Extra attributen zijn nodig op niveau van Notificatiebericht om te linken naar de templates die gebruikt worden om de titel, markup en e-mail body te genereren. **\[UPDATE\]** Voorstel om deze niet expliciet mee op te nemen in het informatiemodel wegens niet relevant voor semantiek en uitwisseling van informatie, louter voor het vormgeven. IDs worden wél bijgehouden in de praktijk in de databases als technische velden.

-   N5: definities voor klassen Bron en Afzender.

    -   De afzender is altijd wat de gebruiker te zien krijgt.

    -   Bij beiden (Bron en Afzender) moet het mogelijk zijn om een dienstverlening uit de dienstverleningscatalogus mee te geven.

    -   De afzender is altijd geassocieerd met een bron, waarbij de bron een officiële publieke organisatie is (i.e. met Wegwijs ID). Tussen beiden is er een many-to-many relatie.

    -   Tijdens de configuratie zet de partner de bron op en creëert dan ook de verschillende afzenders.

    -   Bijgevolg is er ook een relatie nodig tussen Bron en Afzender, bovenop de relaties tussen Notificatiebericht en Bron en Afzender.

    -   Bij Sender moet het mogelijk zijn een e-mailadres mee te geven. Het attribuut isTeBereikenOp zal worden toegevoegd.

    -   **\[UPDATE\]** na verdere analyse van schema.org en op basis van de discussie tijdens het overleg hebben we gekozen om als "Bron" de klasse "PubliekeOrganisatie" te nemen en voor de "Afzender", het schema.org concept "Merk" ([http://schema.org/Brand](http://schema.org/Brand)). Het gebruik hiervan is semantisch consistent met de use cases zoals uiteengezet tijdens het overleg, namelijk dat de afzender steeds de entiteit is die de bestemmeling van een notificatie te zien krijgt (cfr. het "from" field in e-mail). De voorgestelde definitie voor merk is: *"De naam gebruikt door een Publieke Organisatie om te communiceren over een bepaalde Publieke Dienstverlening."*

-   N6: initiatieven als eBox bestaan parallel met de Notificatiecomponent en kunnen indien gewenst er gebruik van maken.

-   N7: notificatieprofiel versus Burgerloket profiel

    -   Voor de gebruikers is er geen verschil. De informatie die binnen de notificatie component getoond wordt zal samen met de andere profielinformatie op dezelfde pagina verschijnen. Het is enkel de plaats waar de gegevens worden opgeslagen die verschilt.

-   N8: e-mailbeheer binnen notificatiecomponent.

    -   Het volstaat om aan de bestemmeling ("Agent") e-mail adressen te kunnen meegeven.

Besluit en acties
=================

1.  Jens en Michiel updaten model o.b.v. discussie

2.  Updated model wordt voorgelegd aan werkgroep ter validatie. Voorlopig lijkt geen nieuw overleg nodig.

3.  Van zodra het model is goedgekeurd stellen Jens en Michiel de nodige documentatie op, analoog aan het specificatiedocument dat voor transactionele dienstverlening (DOSIS) werd gemaakt.
