**Informatie Vlaanderen**

Tweede werkgroep OSLO² Persoon en Burgerloket - U en Uw Gezin

Datum: 23/02/17 -- 10:00 -- 12:00

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: An Boes, Valère Bouserie, Michiel De Keyzer, Jens Scheerlinck,
Annelies De Craene, Nikolaos Loutas, Omaar Verack

Verontschuldigd: Katrien Desmet, Dries Beheydt, Raf Buyle, Bruno De
Vrieze, Philip Boivin

Verslaggever: Jens Scheerlinck

Bijlagen: laatste versies van [de mapping U en Uw Gezin - OSLO²
Persoon](https://docs.google.com/spreadsheets/d/1WMZhT5OjQDDiU08RthLOG6nV7ydPRGQ0RPu9SeffO9E/edit?usp=sharing),
[het voorgesteld datamodel voor U en Uw
Gezin](https://drive.google.com/open?id=0B3DdQTFc4B-VMVdWVlpXTGswMmM),
[voorbeeldbestanden JSON-LD op basis van MAGDA
output](https://drive.google.com/open?id=0B3DdQTFc4B-VNUJRa0VnemRQQ2M)
en [de actielijst van de
werkgroep](https://docs.google.com/spreadsheets/d/1HHOiowsu6Y1d6LEQWedB2uksWoShpsNXk8GgSkIY8OI/edit?usp=sharing).

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Het doel van deze tweede werkgroep is om alle open actiepunten trachten
af te ronden en een aantal nieuwe acties te definiëren die de
semantische afstemming tussen U en Uw Gezin en OLSO² Persoon verankeren.

Verloop
=======

-   Agenda

1.  Bespreken van de voorstellen, vragen en acties op basis van de actielijst.

2.  Overlopen van de semantische mapping tussen OSLO² Persoon en Burgerloket "U en Uw Gezin".

3.  Bepalen van volgende stappen.

-   Michiel en Jens overlopen de manier van werken die gevolgd werd sinds de eerste werkgroep. De volgende artefacten zijn beschikbaar via Google Drive:

    -   Een up-to-date versie van de actielijst die ook de uitkomst aangeeft van zaken die intussen besproken zijn met Geert i.v.m. OSLO² Persoon: [https://docs.google.com/spreadsheets/d/1HHOiowsu6Y1d6LEQWedB2uksWoShpsNXk8GgSkIY8OI/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1HHOiowsu6Y1d6LEQWedB2uksWoShpsNXk8GgSkIY8OI/edit?usp=sharing)

    -   De meest recente versie van de mapping op basis van de recentste informatiebehoefte voor U en Uw Gezin en de laatste versie van het OSLO² Persoon model: [https://docs.google.com/spreadsheets/d/1WMZhT5OjQDDiU08RthLOG6nV7ydPRGQ0RPu9SeffO9E/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1WMZhT5OjQDDiU08RthLOG6nV7ydPRGQ0RPu9SeffO9E/edit?usp=sharing)

    -   Een nieuwe versie van het UML diagram voor U en Uw Gezin: [https://drive.google.com/open?id=0B3DdQTFc4B-VMVdWVlpXTGswMmM](https://drive.google.com/open?id=0B3DdQTFc4B-VMVdWVlpXTGswMmM)

    -   Voorbeelden van JSON-LD files voor GeefPersoon op basis van de XML voorbeelden in de MAGDA documentatie: [https://drive.google.com/open?id=0B3DdQTFc4B-VNUJRa0VnemRQQ2M](https://drive.google.com/open?id=0B3DdQTFc4B-VNUJRa0VnemRQQ2M)

<!-- -->

-   Bespreken van de voorstellen, vragen en acties op basis van de actielijst.

    -   UUG14 Identiteitsbewijzen no match met OSLO²

        -   Verschillende identiteitsbewijzen zijn in-scope van Burgerloket: eID, Kids ID, Vreemdelingen ID en reispas. Naast het rijksregister blijven ook het BIS en RAD register in-scope. De identiteitsbewijzen worden gemodelleerd als output van een Dienstverlening en verschuiven naar de scope van Lopende Dienstverlening.

        -   Wat betreft het BIS register kunnen zowel personen die toegevoegd werden op federaal als Vlaams niveau een login aanvragen voor Burgerloket.

        -   BIS register kan ook speciale gevallen omvatten zoals een zaakvoerder van een buitenlands bedrijf die hier een vestiging heeft of mensen met een onroerende eigendom in België, zonder dat ze hier werken.

    -   UUG7 Geen identificator voor persoon in de analyse-tabellen.

        -   INSZ is geen persistente identificator op zich. Bv. personen die geslachtsverandering hebben ondergaan ontvangen nieuw INSZ nummer. Een koppeling tussen oud en nieuw bestaat maar dit wordt niet gepubliceerd of vrijgegeven. In RR is de link IT002. Ook iemand die eerst in het BIS register werd ingeschreven en daarna inwoner wordt krijgt een nieuw INSZ nummer.

        -   Bij wijziging van het INSZ nummer worden mutaties verstuurd naar de verschillende instanties, welke vervolgens de nodige aanpassingen maken in hun systemen.

        -   Wanneer via MAGDA een oud INSZ nummer wordt opgevraagd dat niet meer in gebruik is, wordt in de response het nieuw INSZ nummer meegegeven.

        -   Valère en An geven aan dat in het kader van een project voor FOD Financiën, er een 'super identifier' werd gebouwd voor personen.

        -   De discussie rond persistente identifier is specifiek in de scope van Burgerloket en U en Uw Gezin niet heel belangrijk aangezien er altijd vanuit de burger vertrokken wordt en deze wel zijn relevante INSZ op dat moment kent en gebruikt EN de link met oude INSZ nummers sowieso ergens wordt bijgehouden. Het is echter wel belangrijk om een globaal zicht te krijgen op een persoon onafhankelijk of deze andere INSZ nummers gekregen heeft, bvb. in het kader van strafzaken, financiën\...

    -   UUG3 Wat met extra elementen voor \"KBI\"? Momenteel nog \"te analyseren\" + link met concept \"Vreemdeling\"?

        -   KBI verhuist volledig naar het domein Onderwijs en valt dus buiten de scope van 'U en Uw Gezin'.

    -   UUG15 GeregistreerdPersoon als centraal object in U en Uw Gezin

        -   Consensus dat GeregistreerdPersoon (en Inwoner) uit OSLO² alle personen die binnen de scope van U en Uw Gezin afdekt.

    -   UUG4 Implementatie van concept \"Vreemdeling\", extensie bovenop OSLO²?

        -   Met het wegvallen van het wachtregister is het niet zeker dat dit concept nog nodig is. An update de informatiebehoefte.

        -   In elk geval blijven mensen die vermeld staan in het vreemdelingenregister in-scope. Er is echter onzekerheid of personen die niet in België geboren zijn in het vreemdelingenregister vermeld blijven of verhuizen naar het bevolkingsregister bij naturalisatie. Valère verifieert dit bij het Rijksregister. Dit heeft niet echt een impact op de modellering maar op vlak van de discussie rond een persistente identifier.

    -   UUG18 \"Wat is de juridische waarde of definitie van een gezin?

        -   Bv. attest van gezinssamenstelling, wordt dit vervaardigd op basis van relaties met de referentiepersoon?\"

        -   Er was consensus dat het object Gezin niet nodig is in het model maar dat duidelijk moet worden gedefinieerd in de specificaties, dat de Gezin gedefinieerd wordt door de associatie isReferentiePersoonVan en zijn inverse

    -   UUG20 Verhouding adres en beheerder

        -   Beheerder bevat de NIS code van de gemeente of consulaire post waar de persoon verblijft.

        -   Voor geradieerden, overledenen, etc. wordt daar een speciale code ingegeven. In MAGDA GeefPersoon worden deze speciale codes weergegeven onder de \"status\" van een persoon.

        -   ToekomstigBeheerder bestaat niet als informatietype in het Rijksregister en is niet nodig binnen Burgerloket. Jens en Michiel kijken na met Geert Thijs of dit moet behouden blijven in OSLO².

    -   UUG21 Relatie Persoon - Adres

        -   Een generieke relatie tussen Persoon en Verblijfsobject waar je een type kan achter steken met een codelijst zal worden opgezet in het data model voor U en Uw Gezin. Jens en Michiel kijken ook na met Geert of deze wijziging ook in OSLO² wordt doorgevoerd of dat dit een extensie blijft binnen Burgerloket.

    -   UUG22 Woonvorm en UUG23 Codelijst plaatsInHetGezin

        -   Valère zal documentatie/use cases/voorbeelden communiceren in verband met \"woonvorm\" om te kunnen evalueren of dit nodig is als afzonderlijk attribuut (of dat dit omvat zit in positie ten opzichte van referentiepersoon o.i.d.).

    -   UUG19 Hoe technische vertaling xml Magda naar Burgerloket?

        -   Jens en Michiel plannen meeting met David Van Den Brande in verband met de richtlijnen die opgesteld werden rond het gebruik van JSON. Daarnaast stemmen Jens en Michiel ook af met Raf Buyle en de technische lead voor WWOOM.

-   Overlopen van de semantische mapping tussen OSLO² Persoon en Burgerloket "U en Uw Gezin".

    -   Waar een 'exact match' wordt aangegeven zal de OSLO² terminologie worden overgenomen na validatie door de Werkgroep (doel: afronden in volgende werkgroep).

    -   An (en Valère) kijken de correctheid van de mapping na;

    -   Jens en Michiel voegen volgende zaken toe aan het voorgesteld data model voor U en Uw Gezin: cardinaliteiten en uitsplitsing samengevoegde datatypes. Daarnaast worden enkele zaken opgenomen met Geert Thijs voor afstemming met OSLO² (zie actie 5).

-   Bepalen van volgende stappen.

Besluit en acties
=================

1.  Valère en An leveren documentatie aan in verband met de 'super
    identifier' die werd gecreëerd voor FOD Financiën.

2.  Valère en An kijken de correctheid van de mapping na.

3.  OSLO² "GeregistreerdPersoon" wordt beschouwd als het centraal
    concept voor persoon binnen Burgerloket.

4.  An update de informatiebehoefte m.b.t. het wegvallen van het
    wachtregister uit de scope tegen 03/03.

5.  Valère verifieert bij het Rijksregister of personen die niet in
    België geboren zijn bij naturalisatie in het vreemdelingenregister
    vermeld blijven of verhuizen naar het bevolkingsregister.

6.  Valère bezorgt informatie over de Woonvorm opgenomen in het RR en
    Magda.

7.  Jens en Michiel spreken volgende zaken af met Geert Thijs in verband
    met het OSLO² persoonsmodel:

    -   Of het nodig is om de relatie "heeftToekomstigBeheerder" te behouden.

    -   Generieke relatie tussen GeregistreerdPersoon en een adres (attribuut met datatype en/of relatie met verblijfsobject).

    -   Juridisch statuut als nieuw type in MAGDA (bestond al langer in het Rijksregister). Is het nuttig om dit toe te voegen aan OSLO² Persoon, aangezien dit ook relevant is voor onder meer Kind & Gezin.

    -   Attribuut nationaliteit met datatype 'Nationaliteit' (NISCode, DatumBegin) binnen Burgerloket. Nuttig om dit binnen OSLO² breder te laten?

8.  Jens en Michiel bespreken de impact van U en Uw Gezin op het model rond Dienstverlening (specifieke outputs zoals verschillende identiteitsbewijzen, bewijsstuk geboorte) met Thomas

9.  Jens en Michiel plannen meeting met David Van Den Brande in verband met de richtlijnen die opgesteld werden rond het gebruik van JSON. Daarnaast stemmen Jens en Michiel ook af met Raf Buyle en de technische lead voor WWOOM.

10. Op basis van de input uit voorgaande acties updaten Jens en Michiel het U en Uw Gezin datamodel, de mapping met OSLO² Persoon en het JSON-LD voorbeeldbestand.

11. De volgende werkgroep werd ingepland voor 09/03/2017, 10u30-11u30 in het Boudewijngebouw te Brussel.
