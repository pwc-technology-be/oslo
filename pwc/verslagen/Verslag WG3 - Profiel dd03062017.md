**Informatie Vlaanderen**

Werkgroep OSLO² en "Profiel"

Datum: 03/06/2017 -- 15:00 -- 16:00

Locatie: Boudewijngebouw Brussel

Aanwezig: Philip Boivin, Omaar Verack, Michiel De Keyzer

Verslaggever: Michiel De Keyzer

Bijlagen:

-   [UML Model](https://drive.google.com/open?id=0B8SEyUR0B9eQMThJRVhSRlZEZE0)

-   [Actielijst](https://docs.google.com/spreadsheets/d/1DldTpOvyuOtpVkNm4lvleXLTI68PjAAGFE_RC4CdKNc/edit?usp=sharing)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Een derde werkgroep overleg rond het Burgerloket \"Profiel" met als doel
het voorstellen van een geüpdate model, op basis van feedback uit het
eerste overleg, het toetsen aan use cases en uitklaren van openstaande
items in de actielijst.

Agenda:

1.  Voorstelling van het updated model

2.  Overlopen en bespreken van punten in de actielijst

Verloop
=======

-   De werkgroep overloopt de het UML model en de belangrijkste wijzigingen die hierbij zijn aangebracht na overleg.

    -   Het verwijderen van de account informatie aangezien dit in scope zit van ACM/IDM en buiten de scope van Burgerloket Profiel zal vallen.

    -   Het toevoegen van een aantal attributen, waarvan een aantal nog te bespreken zijn als onderdeel van het overlopen van de actielijst.

-   De werkgroep overloopt en bespreekt de openstaande punten in de actielijst:

    -   PR6 met betrekking tot de contactvoorkeuren

        -   Er is beslist dat de contactvoorkeuren buiten de scope van het profiel vallen

    -   PR16 codelijst voor aanspreekvorm (attribuut van datatype Contactinfo)

        -   Het voorstel van Jens en Michiel is om hiervoor een codelijst te voorzien. Philip zal dit opnemen in het kader van BT-106. Een placeholder voor de codelijst werd in het model voorzien

    -   PR17 met betrekking tot het opnemen van verschillende adressen:

        -   Er wordt beslist dat dit kan opgevangen worden door verschillende instantiaties van het attribuut isTebereikenOp. Dit attribuut wordt beschreven door een complex datatype ContactInfo.

        -   Wel wordt de nood geformuleerd om aan het datatype ContactInfo een Type toe te voegen zodat dit kan geclassificeerd worden. Hier zal nog een codelijst voor worden uitgewerkt in de toekomst. Voor de codelijst wordt eveneens reeds een placeholder voorzien.

        -   We willen hierbij wel nog beklemtonen dat het niet de bedoeling is om Domicilie informatie via het attribuuut isTebereikenOp te capteren. het Domicilie heeft een wettelijk karakter en is het adres dat als dusdanig in het Rijksregister geregistreerd staat en mag geen andere invulling krijgen.

    -   PR20 coördinaten meenemen voor de adresinfo

        -   Indien de adresstructuur van OSLO gevolgd wordt (wat voorzien is in het huidige model voor Profiel) kan dit via CRAB-LOD gemakkelijk opgehaald worden en moet er verder niets voorzien worden.

    -   PR22, PR24 en PR25

        -   Omaar neemt nog voor volgende attributen nog op of deze al dan niet in scope moeten genomen worden van het model voor Profiel:

            -   Geslacht

            -   adelijkeTitel

            -   bankgegevens

    -   PR23 met betrekking tot een codelijst voor taalType

        -   Michiel en Jens stellen voor om hiervoor een codelijst te voorzien;

        -   Er wordt bevestigd dat dit in de toekomst zal bekeken worden, maar momenteel buiten scope valt.

Besluit en acties
=================

1.  Philip bekijkt de noodzaak en invulling
    voor een codelijst voor aanschrijfvorm;

2.  Omaar bekijkt of volgende attributen al
    dan niet mee in scope van het profiel moeten opgenomen worden:

    -   adelijkeTitel

    -   geslacht

    -   bankgegevens

3.  Jens en Michiel passen de documentatie van
    het model en de voorbeelden in JSON-LD aan
