**Informatie Vlaanderen**

Werkgroep OSLO² en "Profiel"

Datum: 24/04/2017 -- 11:00 -- 12:30

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Philip Boivin, David Van den Brande, Omaar Verack, Annelies De
Craene, Michiel De Keyzer, Jens Scheerlinck

Verontschuldigd: Roeland Tegenbos, Karin Wouters

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [UML Model](https://drive.google.com/open?id=0B3DdQTFc4B-VZHFtY3ZqeVVlaG8)

-   [Actielijst](https://docs.google.com/spreadsheets/d/1DldTpOvyuOtpVkNm4lvleXLTI68PjAAGFE_RC4CdKNc/edit?usp=sharing)

-   [Mapping](https://docs.google.com/spreadsheets/d/10eXr850PpQf257Jupkkn02VviIUkk5IxTOEnkQX4G68/edit?usp=sharing)

-   [Slide deck](http://drive.google.com/open?id=1yt5Vkkvv6DB55yA6MacadoQgXwsFvi2w3gY3h_TjzBc)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Een tweede werkgroep overleg rond het Burgerloket \"Profiel" met als
doel het voorstellen van een geüpdate model, op basis van feedback uit
het eerste overleg, het toetsen aan use cases en uitklaren van
openstaande items in de actielijst.

Agenda:

1.  Stand van zaken -- analyse velden profiel

2.  Voorstelling van het updated model

3.  Toelichting hoe het model de use cases dekt op semantisch en technologisch vlak (o.a. rond het koppelen van profielen)

4.  Overleg rond open functionele/technische/organisatorische vragen

5.  Overlopen en bespreken van punten in de actielijst

Verloop
=======

-   De werkgroep overloopt de Excel lijst met velden die in-scope zijn voor het Burgerloket Profiel op korte én lange termijn (2017+2018).

    -   Bij telefoonnummer, e-mail en adres: toevoegen van veld voor "geprefereerd telefoonnummer" of "voorkeurstelefoonnummer".

    -   Voor het zwak authenticeren van gebruikers wordt momenteel gekeken naar de vo\_idv sleutel van ACM/IDM.

    -   Hoewel contactvoorkeuren zullen uitgewerkt en opgeslagen worden in het domein van notificatie, zijn dit wel zaken die aan de burger zullen getoond worden onder het domein "profiel". De desbetreffende klassen en attributen zullen dus ook worden weergegeven als onderdeel van het profiel in de user interface. De voorkeuren die op niveau van profiel getoond worden moeten functioneel kunnen ingezet worden om alle andere contactgegevens te overrulen.

    -   Algemene voorwaarden: juridische vereisten moeten met Nathalie De Jaeger en Stefanie Kerkhofs afgestemd worden. Kan dit vanuit ACM/IDM toegangsbeheer en cookiebeleid meegenomen worden of moet elke website dit decentraal doen? Consensus om niet mee op te nemen in model omdat dit telkens applicatie gebonden zal zijn.

-   De werkgroep overloopt en bespreekt het voorgestelde informatiemodel en de (JSON-LD) voorbeelden.

    -   Zowel consents als algemene voorwaarden hoeven niet mee opgenomen te worden in dit canoniek model aangezien deze domein- en applicatie-specifiek zijn.

    -   Het attribuut taal wijzigen naar "voorkeurstaal" om semantisch beter overeen te stemmen met de beoogde use cases. Op termijn kunnen daarnaast "taal voor officiële communicatie" en "moedertaal" nodig zijn. Voorlopig zijn hier geen use cases voor.

    -   Het "aanmelden met Burgerloket Profiel" zit niet in het traject vervat. Indien er een generiek, centraal profiel komt zal dit voorzien worden door Toegangsbeheer.

    -   Via de eigenschap "holdsAccount" kan een profiel gelinkt zijn aan meerdere accounts, maar kunnen ook meerdere profielen gelinkt zijn aan dezelfde account.

-   De werkgroep overloopt en bespreekt de openstaande punten in de actielijst:

    -   PR9 en PR10 met betrekking tot thema's

        -   Michiel oppert om thema\'s onder te brengen als eigenschappen van de klasse "persoon" omdat het interesses zijn van die persoon.

        -   Thema's zitten in transversale component van dienstverlening op maat. Afhankelijk van hoe generiek deze worden gedefinieerd zullen ze al dan niet geschikt zijn om te hergebruiken in dit canoniek model voor gegevensuitwisseling.

        -   Discussie blijft on-hold tot hier meer duidelijkheid over is.

    -   PR13 attribuut "rol"

        -   De werkgroep bereikt consensus dat de eigenschap "rol" context en applicatie gebonden is en daarom niet mee zal opgenomen worden in het canoniek informatiemodel voor profiel.

Besluit en acties
=================

1.  Philip, David en Omaar werken use cases
    uit op basis van de PI planning (zowel voor 2017 als 2018) waaraan
    het model kan getoetst worden en delen deze met Michiel en Jens.

2.  Jens en Michiel werken JSON-LD voorbeelden
    en indien nodig andere documentatie uit om het model te toetsen aan
    de use cases, volgens de vooropgestelde prioriteit voor wat betreft
    de implementatie van de use cases (2017, 2018, ter discussie in het
    transversale traject). Hiervoor zal een vervolgmeeting worden
    opgezet om de resultaten van de toetsing te bespreken.

3.  De voorbeelden in JSON-LD worden
    doorgestuurd naar het technische team en indien nodig wordt een
    meeting opgezet om dit te bespreken.

4.  Jens en Michiel bezorgen de vragen die
    betrekking hebben op het functionele, technische en organisatorische
    vlak, maar geen impact hebben op het datamodel aan David die dit kan
    meenemen naar het overleg m.b.t. het transversale traject.
