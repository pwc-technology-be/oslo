**Informatie Vlaanderen**

Werkgroep OSLO² en Woonst & Patrimonium

Datum: 04/05/2017 -- 12:30 -- 14:00

Locatie: [Boudewijngebouw](https://www.google.be/maps/place/Boudewijngebouw/@50.8567731,4.3526172,17z/data=!3m1!4b1!4m5!3m4!1s0x47c3c38369503633:0xe176454918e1b130!8m2!3d50.8567731!4d4.3548059?hl=nl)

Aanwezig: An Boes, Annelies De Craene, Ziggy Vanlishout, Veerle Beyaert,
Michiel De Keyzer, Jens Scheerlinck

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Slide deck](https://drive.google.com/open?id=0B3DdQTFc4B-VWl9OTEJCUmw1MmM)

-   [Eerste versie van het UML model op basis van INSPIRE](https://drive.google.com/open?id=0B3DdQTFc4B-VcTgwNWNGN2dSSUk)

-   [Mapping voorgesteld UML model naar OSLO en INSPIRE](https://drive.google.com/open?id=1ag_LFx15aLcjEkjrooquqzUOqzO0wIqq1wuaBDVrMw4)

-   [Up-to-date versie van de actielijst](https://drive.google.com/open?id=1624NydQvWlE114CikxsL4ZR-ZhNqKBFtaRIcVoOeMBM)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

1.  Huidige status OSLO²:

    -   Adres

    -   Gebouw

    -   Perceel

2.  Status Burgerloket

3.  Overlopen informatienoden

Verloop
=======

-   Huidige status OSLO²

    -   Adres

        -   31 maart werden een adres vocabularium en applicatie profiel opgeleverd als onderdeel van het OSLO² traject. Deze werden reeds toegepast in de context van het CRAB-LOD project.

    -   Gebouw

        -   Een gebouwenregister is momenteel in de maak en is gebaseerd op OSLO² Gebouw.

        -   Dit model werd niet opgeleverd op 31/03 samen met de andere vocabularia, vermoedelijk door tijdnood. De aanpassingen die nog moeten gebeuren aan OSLO² Gebouw zijn vooral vormelijk maar ook inhoudelijk moet nog gedeeltelijk een terugkoppeling gebeuren vanuit het model van gebouwenregister.

        -   Het gebouwenregister heeft als scope alle gebouwen.

        -   Een Beta versie van de gebouwenregister web service is reeds beschikbaar. De bedoeling is dat dit later zal dit geïntegreerd worden in de MAGDA service.

        -   Gebouwenregister team zal laatste versie van het gebruikte informatiemodel doorsturen met extra attributen die in acht worden genomen.

        -   In de context van Burgerloket zal ook de informatie mee opgenomen worden van het \"Woningpas\" project. Dit project heeft als doel het samenbrengen van alle partijen die administratieve gegevens hebben m.b.t. over een woning willen ontsluiten. Een eerste light versie zou klaar moeten zijn tegen Batibouw 2018. PwC vraagt als actiepunt via het Burgerloket team op of er reeds documentatie bestaat rond het datamodel of informatiebehoeften van Woningpas.

        -   Het attribuut geldigheidsPeriode in OSLO² Gebouw en het gebouwenregister komt overeen met het concept lifeCycleInfo uit INSPIRE.

    -   Perceel

        -   Momenteel bestaat er een voorstel om een percelenregister te maken, de verdere ontwikkeling van OSLO² Perceel zal daarvan afhangen.

        -   Bedoeling is het creëren van een buffer databank die informatie ontsluit met behulp van OSLO semantiek, maar zelf niet aan gegevensinwinning doet.

        -   Percelenregister zou een combinatie worden van kadastrale percelen (sec percelen, focus op geometrie) en eigendommen.

        -   MAGDA bevat momenteel alleen informatie over eigendommen (niet geografische informatie) uit de kadastrale legger.

-   Status Burgerloket en overlopen informatienoden.

    -   Aard van het perceel: onzeker of we dit willen tonen (eerder niet dan wel).

    -   Kadaster informatie wordt ingewonnen bij een goederenrechtelijke actie (bv. akte bij notaris), verder zijn er geen bijhoudingsprocessen.

    -   Kadastraal inkomen wordt beschreven aan de hand van:

        -   Lettercode en cijfercode: beschrijvend

        -   Sleutel purtoestand: patrimoniaal perceel (partitienummer), dit is niet de grond maar de identificatie van de eigendom, slaat meer op het gebouw dan op het perceel.

    -   Liggingsadres wordt beschouwd al een attribuut met type \"adresvoorstelling\", een apart project voor koppeling met CRAB adressen zal worden opgestart. In deze context zijn er een aantal opmerkingen:

        -   Wat met adressen die gewijzigd zijn na registratie?

        -   Koppeling tussen perceel en adres is nog steeds verantwoordelijk van kadaster?

        -   Gemeente is verantwoordelijk om adressen te koppelen aan gebouweenheden.

        -   Momenteel geen proces binnen kadaster dat rekening houdt met wat gemeenten doen. Er is momenteel geen bijhoudingsproces.

    -   In de context van (terug)meldingen is er nood aan overleg met Carolien Willen over hoe dit af te handelen, bv. in het kader van gebouwen of adressen. Voor informatie uit het kadaster is het mogelijk dat de informatie niet up-to-date is of informatie over de koppeling met adres ontbreekt (verantwoordelijkheid van adressenregisters). Momenteel werd nog niet bekeken hoe koppelingen gaan bijgehouden worden.

    -   Voor Waalse en Brusselse eigendommen zal maar beperkte informatie worden meegegeven door beperkte beschikbaarheid van data.

    -   Zakelijk recht:

        -   APD gegevens (niet VLABEL), vooral een percentage en type recht.

        -   Voor mede-eigenaren wordt enkel het aantal mede-eigenaren getoond.

        -   Bv. bij getrouwde koppels beiden 100% eigenaar maar elk 50% \"rechten\".

        -   \'Afpaling\' -\> niet helemaal duidelijk wat dit is.

    -   Energiegegevens: momenteel is de consensus om dit niet op te nemen omdat het niet duidelijk is van waar deze gegevens komen. Kadaster verstuurd mogelijks brief naar eigenaars bij aankoop/verkoop waarin deze informatie zit. Wordt nagevraagd bij kadaster of dit wordt gebruikt... Indien wél -\> opnemen en duidelijk vermelden van bron. In elk geval dient dit eerst afgestemd te worden met het VEA.

    -   Status eigendom: niet duidelijk wat dit momenteel juist is.

    -   Bronnen voor de onzekere gegevens zijn VEA (energiegegevens), adressenregister (status eigendom) en gebouwenregister (mede-eigenaars).

    -   Moeten gebouwen in opbouw of aangevraagd getoond worden in Burgerloket onder "Woonst & Patrimonium"? Bijvoorbeeld gebouwen die wel al ingetekend werden in het gebouwenregister maar nog geen écht gebouw zijn in realiteit.

    -   AAPD heeft informatie m.b.t. kavel en liggingsadres. Als voor een gegeven lliggingsadres al een gepland gebouw is opgenomen in het gebouwenregister kan reeds informatie over dit gebouw worden opgevraagd bij het gebouwenregister. Veerle gaat deze use case bekijken wanneer koppeling getest wordt (wat te doen met geplande gebouweenheden). Hieromtrent werd verder besproken om het concept of de term van "hoedanigheid" niet te gebruiken in het model.

Besluit en acties
=================

1.  An Boes deelt MAGDA documentatie rond Percelen en Eigendommen met de werkgroep.

2.  Analyse informatiemodel dient klaar te zijn voor 26/05 aangezien daarna de ontwikkeling start binnen Burgerloket.

3.  Gebouwenregister team deelt laatste versie van informatiemodel met de werkgroep.

4.  Veerle Beyaert neemt bij het testen van de gebouwenregister koppeling de use case rond het al dan niet tonen van geplande (maar niet gerealiseerde) gebouwen mee in acht.

5.  Werkgroep bespreekt met GTMF/digimelding team (Carolien Willen) de impact van terugmeldingen op gebouwen en adressen, meer bepaald hoe deze worden afgehandeld door het systeem.

6.  In het informatiemodel zal de scope liggen op de huidige toestand van een perceel/gebouw, lifecycle informatie zal dus niet getoond worden.

7.  PwC vraagt via Burgerloket (Annelies/An) of er reeds informatiebehoeften of een datamodel beschikbaar is van Woningpas.

8.  Het volgend overleg wordt gepland op 16/05 van 12:30 tot 14:00.
