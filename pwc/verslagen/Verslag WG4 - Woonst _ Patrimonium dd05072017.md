**Informatie Vlaanderen**

Werkgroep OSLO² en Woonst & Patrimonium

Datum: 05/07/2017 -- 13:30 -- 15:00

Locatie: [Boudewijngebouw & VAC
Gent](https://www.google.be/maps/place/Boudewijngebouw/@50.8567731,4.3526172,17z/data=!3m1!4b1!4m5!3m4!1s0x47c3c38369503633:0xe176454918e1b130!8m2!3d50.8567731!4d4.3548059?hl=nl)

Aanwezig: An Boes, Annelies De Craene, Veerle Beyaert, Ziggy Vanlishout,
Michiel De Keyzer, Jens Scheerlinck

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Voorgesteld UML model](https://drive.google.com/open?id=0B3DdQTFc4B-VRjUydC1sSGhhNTg)

-   [Up-to-date versie van de actielijst](https://drive.google.com/open?id=1624NydQvWlE114CikxsL4ZR-ZhNqKBFtaRIcVoOeMBM)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Vierde werkgroep overleg rond de afstemming van het Burgerloket Mijn
Woonst en Patrimonium en de OSLO² vocabularia. De bedoeling van dit
overleg is om de laatste actiepunten te sluiten en het model af te
kloppen.

Verloop
=======

-   De klasse Eigendomstoestand blijft behouden om de eigenschap 'aantalMedeEigenaars' mee te geven. Daarnaast zorgt dit er ook voor dat de structuur grotendeels in lijn blijft met die van MAGDA.

-   Gebouwenregister team gaat in MAGDA een link toevoegen van PatrimoniaalPerceel naar Gebouweenheid, waardoor deze relatie expliciet (met de bijhorende identificator) kan opgenomen worden in de Burgerloket service.

-   Via aparte call kan dan de identificator van het Gebouw worden opgevraagd dat aan de Gebouweenheid is gelinkt. Bouwjaar kan daar getoond worden.

-   Het attribuut 'bouwjaar' is momenteel nog niet opgenomen in gebouwenregister, maar er is beslist dat dit er wel zal komen. Voorlopig kan het bouwjaar van AAPD via MAGDA als waarde genomen worden voor dit attribuut totdat het beschikbaar is via gebouwenregister.

-   De relatie tussen PatrimoniaalPerceel en Gebouweenheid moet bepaald worden als zero-to-many in beide richtingen.

-   Geometrieën zullen opgevraagd worden bij GRB en gebouwenregister, de x,y coordinaten van AAPD die via MAGDA ontsloten worden zullen niet worden gebruikt. Voor Gebouw is dit een geometrie die wordt bijgehouden door het gebouwenregister. De identificator om dit op te halen is de CaPaKey.

-   Authentieke adressen en adres voorstellingen kunnen ook opgehaald worden bij CRAB/Gebouwenregister/GRB of BEST (voor adressen buiten Vlaanderen) door gebruik te maken van deze identificator.

Besluit en acties
=================

1.  Bouwjaar zal worden opgenomen als eigenschap van Gebouw in het gebouwenregister.

2.  Geometrieën zullen opgevraagd worden bij GRB en gebouwenregister

3.  Adressen worden ook rechtstreeks bij de authentieke bronnen opgehaald.

4.  An Boes bezorgt voorbeelden van MAGDA output aan Jens en Michiel, zij anonimiseren de data voor gebruik als voorbeelden in de specificatiedocumenten.

5.  OSLO/Gebouwenregister team evalueert welke delen van het model kunnen meegenomen worden in OSLO/Gebouwenregister.

6.  PwC voert besproken wijzigingen door in UML diagram en maakt op basis hiervan de nodige specificatiedocumenten aan, inclusief JSON-LD voorbeelden.
