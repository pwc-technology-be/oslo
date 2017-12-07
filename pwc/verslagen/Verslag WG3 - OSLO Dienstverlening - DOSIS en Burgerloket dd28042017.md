**Informatie Vlaanderen**

Werkgroep OSLO² Dienstverlening en Burgerloket DOSIS

Datum: 28/04/2017 -- 10:30 -- 12:00

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Thomas D'haenens, Bart Misseeuw, Goedele Van der Spiegel, Raf
Buyle, Dries Beheydt, Dorien Bauwens, Michiel De Keyzer, Jens
Scheerlinck

Verontschuldigd: Katrien Mostaert, Nikolaos Loutas, Ziggy Vanlishout

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Verslag van de de laatste vergadering](https://drive.google.com/open?id=1DyT6eIptdiTW3u2o8mx3fyUdLs5_l9agKOL37fCB31o)

-   [Nieuwe versie van het UML model op basis van de ontvangen feedback](https://drive.google.com/open?id=0B3DdQTFc4B-VTnZkSG1WQm1MYjA)

-   [Mapping voorgesteld UML model naar DOSIS model](https://docs.google.com/spreadsheets/d/12aKDZjPIgJoIlJ6v5rs2Uni1jw_yqu5wcS4MFUCWGEI/edit?usp=sharing)

-   [Up-to-date versie van de actielijst](https://drive.google.com/open?id=1UeVfgAygXyE4Z0339XKrVjbqg1pMB1CHqkLiFK21ABk)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

-   Presenteren van nieuwe versie van het informatiemodel voor transactionele dienstverlening in het kader van OSLO² compliant gegevensuitwisseling voor Burgerloket.

-   Afkloppen van updated model en sluiten van resterende open actiepunten.

Verloop
=======

-   Bespreking van het informatiemodel

    -   Op basis van input van het tweede werkgroepoverleg werd de specifieke klasse voor "Transactie" geschrapt. De klasse PubliekeDienstverlening beschrijft de specifieke dienstverlening die wordt afgenomen door de burger. Volgende eigenschap worden opgenomen:

        -   naam: de naam van de publieke dienstverlening (bv. stedenbouwkundige vergunning, verplicht veld).

        -   beschrijving: een tekstuele beschrijving van de specifieke dienstverlening (optioneel veld).

        -   contactinfo: de contactinformatie die betrekking heeft op deze specifieke dienstverlening (bv. de contactinformatie van de dossierbeheerder of een doorverwijzing (URL) naar een extern platform, optioneel veld).

        -   kost: de kostprijs die de burger betaalt voor het afnemen van deze dienstverlening (dit wordt een optioneel veld).

        -   sector: sectorinformatie met NACE als mogelijke classificatie. Het gebruik van andere classificaties in de plaats van of als aanvulling van de NACE codes zijn mogelijk (optioneel veld, meerdere waarden mogelijk).

        -   taal: de taal waarin de specifieke dienstverlening wordt verleend (optioneel veld).

        -   type: type dienstverlening volgens de COFOG classificatie (optioneel, meerdere waarden mogelijk).

    -   Vanuit de PubliekeDienstverlening klasse vertrekken een aantal relaties naar de klasse 'Agent' (in praktijk: personen, organisaties, publieke organisaties of hoedanigheden) Ter verduidelijking: \'hoedanigheid\' is binnen OSLO² context een persoon die een bepaalde functie heeft bij een organisatie en vanuit deze hoedanigheden handeling stelt.

        -   heeftVerantwoordelijke (cpsv-ap: competent authority): de *publieke organisatie* die de eindverantwoordelijke is voor deze dienstverlening (zoals momenteel gedefinieerd in IPDC als de Bevoegde Overheid, verplicht veld).

        -   wordtUitgevoerdDoor: de Agent (in praktijk: persoon of organisatie of hoedanigheid) die verantwoordelijk is voor het uitvoeren of afleveren van de dienstverlening (optioneel veld, meerdere mogelijk).

        -   heeftParticiperende: generieke relatie voor andere participerende agenten. Voor deze relatie moet verplicht een attribuut 'rol' worden meegegeven en optioneel een beschrijving. De codelijst voor de eigenschap 'rol' werd afgeklopt op: **aanvrager, begunstigde, betrokkene** (participerend agent waarop de diesntverlening betrekking heeft) **en raadpleger** (heeft het recht om informatie met betrekking tot deze publieke dienstverlening te raadplegen). Opnieuw zullen al deze rollen in praktijk worden toegekend aan een specifieke persoon, organisatie of hoedanigheid.

    -   Een extensie bovenop het bestaande OSLO² Dienstverleningsmodel is de eigenschap 'PubliekeDienstverlening' -\> 'heeftStatus' -\> 'Status'. Hierbij is 'Status' een datatype met de eigenschappen van het DOSIS statusobject + de DOSIS dossier-eigenschappen 'isPubliek' en 'isVertrouwelijk'.

    -   Het dosis 'Bron' concept werd gealigneerd met het OSLO concept 'Record', waarbij een 'object' (in dit geval een publieke dienstverlening) beschreven wordt door een record met een bepaalde herkomst (semantisch in lijn met bron). Als extensie werd hier de eigenschap 'statusVlaamseFase' (kardinaliteit 0..\*) aan toegevoegd om toe te laten alle mogelijke Vlaamse fases mee te geven. Door deze alignering wordt een extra vereiste opgelegd: het meegeven van de creatiedatum (eigenschap tijdstip). Deze creatiedatum wordt reeds meegegeven als onderdeel van de eerste status en vormt bijgevolg geen probleem.

-   Bespreking m.b.t. unieke en persistente identificatie van transactionele dienstverlening.

    -   In het kader van communicatie tussen verschillende overheidsentiteiten en de technische communicatie tussen applicaties bestaat er een noodzaak om transactionele publieke dienstverlening uniek en persistent te identificeren, aan de hand van een URI.

    -   Momenteel wordt binnen DOSIS een unieke sleutel gegenereerd door het samenvoegen van volgende velden: {organisatienaam}+{productnaam}+{dossierID}.

    -   De werkgroep stelt de volgende URI voor: [http://data.vlaanderen.be/id/publiekedienstverlening/{wegwijsID}+{productencatalogusID}+{dossierID](http://data.vlaanderen.be/id/publiekedienstverlening/%7BwegwijsID%7D+%7BproductencatalogusID%7D+%7BdossierID)}

    -   Deze kan vandaag reeds geïmplementeerd worden op voorwaarde dat de huidige wegwijs IDs en IPDC IDs behouden zullen blijven in de nieuwe versies van beide registers.

-   Positionering van dit werk binnen het OSLO² domein.

    -   Dit informatiemodel en de specificaties die er voor aangemaakt worden, zullen gehuisvest worden op [http://data.vlaanderen.be/ns/](http://data.vlaanderen.be/ns/) als 'ApplicatieProfiel Transactionele Dienstverlening'.

Besluit en acties
=================

1.  De klasse 'output' wordt mee opgenemen als niet-verplichte klasse in
    het model om future-proof te zijn, net als de concepten kanaal en
    bewijs.

2.  De link tussen bewijs en output moet in de toekomst nog nader
    bekeken worden (maar oefening wordt niet in het kader van
    burgerloket opgenomen aangezien er momenteel geen use case voor is).

3.  Als codelijst voor de eigenschap 'rol' van de klasse 'Participatie'
    worden volgende waarden opgenomen:

    -   Aanvrager

    -   Begunstigde

    -   Betrokkene Voorwerp

    -   Onderwerp

    -   heeftBetrekkingOp

    -   Betreffende (bijvoeglijk naamwoord)

    -   (participerend agent waarop de dienstverlening betrekking heeft)

    -   Raadpleger (heeft het recht om informatie met betrekking tot deze publieke dienstverlening te raadplegen)

4.  Voorstel URI m.b.t. het uniek identificeren van transactionele dienstverlening kan geïmplementeerd worden op voorwaarde dat de huidige wegwijs IDs en IPDC IDs behouden zullen blijven in de nieuwe versies van beide registers. Dit zal worden nagegaan met de desbetreffende aanspreekpunten.

5.  Voorstel m.b.t. URI ter identificatie van transactionele dienstverlening wordt verder besproken in de werkgroep rond URI naamgeving.

6.  PwC neemt contact op met Bert Van Nuffelen voor het publiceren van codelijsten (specifiek deze m.b.t. participatie - rol) op data.vlaanderen.be.

    -   Update: Codelijsten moeten aangeleverd worden aan Bert als een SKOS taxonomie.

    -   Mogelijkheid tot integreren van editor voor eindgebruikers (zodat omzetting naar SKOS taxonomie automatisch kan gebeuren).

    -   Voor het publiceren moet eerst nog een html template worden uitgewerkt, maar kan vrij snel gaan.

7.  Werkgroep valideert de mapping een geeft feedback, in het bijzonder met betrekking tot de kardinaliteiten en welke klassen en eigenschappen al dan niet verplicht worden.

8.  PwC werkt een specificatiedocument uit in HTML (op basis van OSLO² template) inclusief uitgewerkt JSON-LD voorbeeld op basis van DOSIS use case.
