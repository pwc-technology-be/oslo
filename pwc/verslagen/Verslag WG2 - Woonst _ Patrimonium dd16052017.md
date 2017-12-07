**Informatie Vlaanderen**

Werkgroep OSLO² en Woonst & Patrimonium

Datum: 16/05/2017 -- 12:30 -- 14:00

Locatie: [Boudewijngebouw](https://www.google.be/maps/place/Boudewijngebouw/@50.8567731,4.3526172,17z/data=!3m1!4b1!4m5!3m4!1s0x47c3c38369503633:0xe176454918e1b130!8m2!3d50.8567731!4d4.3548059?hl=nl)

Aanwezig: An Boes, Annelies De Craene, Ziggy Vanlishout, Veerle Beyaert,
Michiel De Keyzer, Jens Scheerlinck

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Voorgesteld UML model](https://drive.google.com/open?id=0B3DdQTFc4B-VQ2RzbVdoeGRtNzg)

-   [Up-to-date versie van de actielijst](https://drive.google.com/open?id=1624NydQvWlE114CikxsL4ZR-ZhNqKBFtaRIcVoOeMBM)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Tweede werkgroep overleg rond de afstemming van het Burgerloket Mijn
Woonst en Patrimonium en de OSLO² vocabularia. Tijdens dit
werkgroepoverleg wordt een eerste datamodel voorgesteld gebaseerd op de
OSLO² standaard.

Verloop
=======

-   De werkgroep bespreekt het voorgestelde UML model.

-   Klasse OSLO-Perceel:

    -   Kadastraal inkomen

        -   Kadastraal inkomen krijgt een CaPaKey toegewezen door AAPD.

        -   Het attribuut partitie vormt samen met de CaPaKey de verwijzing naar een instantie van de klasse Gebouweenheid (rechtstreekse relatie tussen Kadastraal Perceel en Gebouweenheid).

        -   Het attribuut kadastraalInkomen verhuist bijgevolg best naar de klasse Gebouweenheid.

        -   Bovenstaande dient bevestigd te worden met mensen van AAPD.

    -   Perceel versus Kadastraal Perceel

        -   Binnen OSLO² slaat de klasse perceel op het geometrisch perceel, waar per locatie maar één instantie kan van bestaan.

        -   In de context van eigendomsrechten wordt gebruik gemaakt van het concept kadastraal perceel. Wanneer de rechtenstructuur van het perceel en de gebouweenheid die erop gevestigd is hetzelfde zijn is er in weze geen verschil tussen een perceel en kadastraal perceel. Echter, waar de rechtenstructuur verschilt tussen perceel en gebouweenheid (bv. Perceel is eigenaar van persoon A, gebouweenheid is eigendom van persoon A en persoon B) zal AAPD voor elke rechtenstructuur een apart kadastraal perceel creëren (wat in het geometrisch perceel valt).

        -   Een bijzonder geval is wanneer er ook verschillende rechten structuren bestaan per verdieping. In dit geval is de opdeling niet enkel te maken op basis van kadastrale percelen. In dit geval wordt een een PatKey gewerkt.

        -   Voor wat betreft het burgerloket is het momenteel enkel nodig om adres informatie m.b.t. het (kadastraal) perceel te tonen wanneer er zich op het perceel geen gebouw(eenheid) bevindt.

        -   Om dit verschil duidelijk te maken zal in het model een nieuwe klasse aangemaakt worden voor Kadastraal Perceel met relaties naar de de klasse Eigendom en Perceel + Gebouweenheid.

-   Klassen Gebouw en Gebouweenheid

    -   De AAPD informatie m.b.t. aantal verdiepen, badkamers, etc. zal niet getoond worden. De bron van deze data is onduidelijk en er zijn geen bijhouding processen.

-   Klasse Eigendom

    -   Voor de naam en definitie van deze klasse kan gekeken worden naar de INSPIRE Cadastral Parcels klasse \"BasicPropertyUnit\".

    -   Momenteel wordt deze uitsluitend gedefinieerd in de context van Kadastrale Percelen, terwijl dit in de context van de Vlaamse Overheid ook kan toegepast worden op Gebouweenheid.

    -   Te onderzoeken of BasicPropertyUnit breder kan getrokken worden om ook toepasbaar te zijn op gebouweenheden (INSPIRE RDF vocabularium momenteel nog in draf/review).

-   De bezorgdheid wordt geopperd dat dit veel extra werk met zich zal meebrengen om te implementeren in Burgerloket.

    -   Veerle en Ziggy leggen uit dat deze initiële investering het makkelijker zal maken om later extra informatie toe te voegen aan Burgerloket die getoond moet worden aan de burger.

    -   Werkgroep beslist dat na update van het model op basis van dit overleg, het Burgerloket team zal aangeven wat voor hen vandaag niet nodig is. Op basis daarvan zal een applicatie profiel ontwikkeld worden dat hier rekening mee houdt op basis van de kardinaliteiten, opdat enkel het nodige geïmplementeerd moet worden.

Besluit en acties
=================

1.  Bezorgen van AAPD slide deck m.b.t. percelen en kadastrale percelen aan werkgroep (Veerle - 22/05/2017 **-\> ONTVANGEN**)

2.  Begrip van kadastraal inkomen en dat het kan verhuisd worden naar de klasse Gebouweenheid in het model bevestigen met AAPD (Annelies en An - 22/05/2017)

3.  Update van UML model op basis van overleg \[Jens en Michiel- 24/05/2017). Hiervoor zal gekeken worden naar INSPIRE voor \'BasicPropertyUnit\' en het onderscheid tussen perceel en kadastraal perceel.

4.  Burgerloket team geeft op basis van updated model aan wat al dan niet relevant is vandaag voor de implementatie (Annelies en An - 29/05/2017)

5.  Vervolgoverleg vindt plaats op 29/05/2017
