**Informatie Vlaanderen**

Werkgroep OSLO² Dienstverlening en Burgerloket DOSIS

Datum: 15/02/2017 -- 13:00 -- 14:30

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Bart Misseeuw, Goedele Van der Spiegel, Katrien Mostaert, Raf
Lauriks, Ziggy Vanlishout, Dries Beheydt, Raf Buyle, Michiel De Keyzer,
Nikolaos Loutas, Jens Scheerlinck

Verslaggever: Jens Scheerlinck

Bijlagen:
[presentatie](https://drive.google.com/file/d/0B3DdQTFc4B-VWXNvT2VIV0FfSkE/view?usp=sharing),
[JSON-LD
voorbeeld](https://drive.google.com/open?id=0B3DdQTFc4B-VSDZuR1h4eW5wakE)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

**Primair**

-   Uitklaren van de terminologie rond lopende dienstverlening, geïnstantieerde diensteverlening, dossier, executiemodel\...;

-   Bepalen van de volgende stappen;

**Secundair**

-   Behandelen van actiepunten voortvloeiend uit de initiële mapping;

Verloop
=======

-   Agenda

1.  Toelichten van voorgestelde aanpak voor verdere afstemming;

2.  Analyse lopende dienstverlening (DOSIS) vanuit Burgerloket en datamodel voor dienstverlening in OSLO² traject;

3.  Uitklaren van de concepten "lopende dienstverlening", "geïnstantieerde dienstverlening", "dossier", "executie model", etc.;

4.  Hoe de executie van dienstverlening in de echte wereld capteren met het datamodel?

5.  Volgende stappen

-   **Toelichten van voorgestelde aanpak voor verdere afstemming**

    -   Michiel presenteert de voorgestelde aanpak bestaande uit: analyse van informatiebehoefte, vertalen in UML model volgens "OSLO²" stijl, mapping opstellen tussen Burgerloket (DOSIS) en OSLO² dienstverlening en finaal het formuleren van concrete acties en voorstellen.

    -   Er zijn geen specifieke opmerkingen op de aanpak;

-   **Analyse lopende dienstverlening (DOSIS) vanuit Burgerloket en datamodel voor dienstverlening in OSLO² traject**

    -   Analyse DOSIS voor burgers grotendeels gebaseerd op DOSIS voor ondernemers dat reeds eerder werd uitgebouwd.

        -   Dit werd al eens getoetst aan OSLO1.

        -   Nu aan het kijken of deze ook fit voor burgers -\> lijkt het geval, mits enkele kleine aanpassingen (maar verhaal blijft hetzelfde).

        -   Momenteel aan het praten met verschillende agentschappen om aan te sluiten op DOSIS

        -   Eind PI1: voor een test rijksregisternummer dossier status kunnen ophalen

        -   DOSIS houdt zich momenteel niet bezig met de output, maar deze output is wel in-scope voor Burgerloket.

    -   OSLO² Dienstverlening

        -   Vertrokken uit use case van catalogus (IPDC).

        -   Sterk hergebruik van CPSV-AP.

        -   Doel is om eind maart te landen met versie 1 van dit model.

        -   Vraag is of dit ook kan toegepast worden op een executie model.

-   **Uitklaren van de concepten "lopende dienstverlening", "geïnstantieerde dienstverlening", "dossier", "executie model", etc. en hoe de executie van dienstverlening in de echte wereld capteren met het datamodel**

    -   Introductie van de term of het concept "transactie" wanneer we spreken over de uitvoering van een dienstverlening.

    -   Semantisch is quasi al het nodige reeds gedefinieerd op niveau van OSLO² Dienstverlening (wat sterk gebaseerd is op CPSV-AP)

    -   Een transactie is dan louter de vertaalslag van die zaken die er nodig zijn vanuit het datamodel OSLO² dienstverlening, naar een formaat voor de captatie van zaken die geïnstantieerd worden. Een eenvoudig voorbeeld hiervan is opgenomen in de presentatie, zowel in tabelvorm als in JSON-LD;

    -   De werkgroep had enkele vragen rond deze manier van werken en sommige zaken dienen nog worden uitgeklaard, echter de werkgroep was akkoord dat deze manier van het kijken naar dienstverlening en het model geschikt was voor wat men in burgerloket wil opzetten. Rond de term "transactie" zelf wordt nog eens nagedacht, maar in principe is dit gewoon een manier om het te benoemen en is dit voor implementatie niet echt belangrijk;

    -   Enkele vragen worden geopperd met betrekking tot de praktische toepasbaarheid van het transactie concept in combinatie met het OSLO² Dienstverleningsmodel:

        -   Meerdere betrokkenen zijn mogelijk in een dienstverleningsdossier, bijvoorbeeld de ouders (aanvragers) van een kind voor wie een studietoelage wordt aangevraagd (betrokkene of begunstigde). Het (OSLO² Dienstverlening) model laat dit toe door middel van het concept 'Participatie'.

        -   Agentschappen hebben aparte beheersystemen, moet de "input" kant van de transactie dezelfde standaarden volgen of moet enkel de output semantisch conform zijn? -\> consensus dat output van grootste belang is maar dat het voor agentschappen die in de toekomst aansluiten logisch zou zijn om meteen aan de "input" kant ook gealigneerd te zijn. Indien dit niet het geval zou zijn, zou men in DOSIS mogelijks een onbeheersbare hoeveelheid verschillende manier van input krijgen (theoretisch mogelijks 308 gemeenten, 5 provincies, alle entiteiten van de Vlaamse overheid)

        -   Gaan andere systemen de \"Output ID\" kunnen lezen? Indien neen -\> niet matuur genoeg om toe te treden.

        -   Moeten zaken als automatisch uitbetalen van kinderbijslag opgenomen worden?

    -   Model moet beschouwd worden als een kader waarin kan gedacht worden en waaruit ook het groter geheel blijkt.

Besluit en acties
=================

1.  Het concept "transactie" werd geïntroduceerd met betrekking tot de
    praktische uitvoering van een dienstverlening. Er was consensus dat
    deze manier van het kijken naar een dienstverlening die geïnitieerd
    werd, geschikt is voor de uitwerking in het kader van Burgerloket;

2.  Jens en Michiel gaan mapping updaten van DOSIS naar OSLO²
    Dienstverlening en resultaten communiceren.

3.  Jens gaat eerste versie van een mogelijke
    JSON-LD file delen met Dries.

4.  Volgende Doodle is opgesteld voor de
    volgende werkgroep:\
    [http://doodle.com/poll/96d32naeix7bkgxw](http://doodle.com/poll/96d32naeix7bkgxw)\
    Bedoeling is om tijdens deze werkgroep door specifieke actiepunten
    en voorstellen te lopen, waarvoor de mapping als basis zal dienen
