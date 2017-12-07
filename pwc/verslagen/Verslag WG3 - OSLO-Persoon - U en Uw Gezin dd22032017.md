**Informatie Vlaanderen**

Tweede werkgroep OSLO² Persoon en Burgerloket - U en Uw Gezin

Datum: 23/02/17 -- 10:00 -- 12:00

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: An Boes, Raf Buyle, Jens Scheerlinck, Annelies De Craene

Verontschuldigd: Katrien Desmet, Dries Beheydt, Bruno De Vrieze, Philip
Boivin, Valère Bouserie, Michiel De Keyzer

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [OSLO² Persoonsmodel](https://drive.google.com/file/d/0B3DdQTFc4B-VZll4V0VOXzY2MEk/view)

-   [Gereviseerde mapping naar OSLO² op basis van de \"U en Uw Gezin\" informatiebehoefte](https://drive.google.com/open?id=1WMZhT5OjQDDiU08RthLOG6nV7ydPRGQ0RPu9SeffO9E)

-   [Up-to-date actielijst](https://docs.google.com/spreadsheets/d/1WMZhT5OjQDDiU08RthLOG6nV7ydPRGQ0RPu9SeffO9E/edit?usp=sharing)

-   [\"Burgerloket Persoon\" model](https://drive.google.com/file/d/0B3DdQTFc4B-VVFp0MG1oNXhBdHc/view)

-   [JSON-LD voorbeeld](https://drive.google.com/open?id=0B3DdQTFc4B-VbVBualYtQzhXMFU)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Het doel van deze derde werkgroep is om alle open actiepunten af te
ronden in het licht van het vernieuwde OSLO² model voor Persoon en het
voorgesteld model voor Burgerloket Persoon af te kloppen.

1.  Voorstelling van het nieuwe OSLO² Persoonsmodel.

2.  Bespreken van open punten in de actielijst.

3.  Valideren van mapping.

4.  Bespreken van Burgerloket Persoonsmodel en vastleggen van eventuele wijzigingen op basis van voorgaande discussies.

Verloop
=======

-   De werkgroep bespreekt het nieuwe OSLO² Persoonsmodel in het licht van de informatienoden voor de domein service "U en Uw Gezin". De volgende vragen, opmerkingen en antwoorden werden geopperd:

    -   Dit OSLO² model voor Persoon werd reed afgetoetst met Fedict (Liesbet D'Hondt) en tijdens een publieke OSLO² werkgroep.

    -   OSLO² voorziet het concept "nationaliteit" maar laat aan de hergebruikers (applicaties) over om hier invulling aan te geven met specifieke attributen. Met andere woorden, OSLO² legt geen attributen op om Nationaliteit te beschrijven.

    -   Persoon wordt gemodelleerd als subtype (subklasse) van het concept "Agent". Via agent als ontkoppelpunt kan Persoon in verband gebracht worden met onder meer dienstverlening, organisatie en hoedanigheid.

    -   Naam wordt gemodelleerd als een eigen concept (klasse) met een aantal subtypes (subklassen) zoals voornaam, achternaam, alternatieve naam, etc. Dit laat toe om naam op verschillende manieren invulling te geven.

    -   Hoe kan de hele gezinssamenstelling worden getoond aan de hand van dit model? Dit zou mogelijk zijn aan de hand van het concept "Gezin" **-\> Jens werkt voorbeeld uit in JSON-LD**

    -   Wat betreft de persoonsrelatie 'Huistvesting' **-\> voorstellen aan Geert om adres toe te voegen als attribuut aan Rijksregister applicatieprofiel. Zo niet, toevoegen aan Burgerloket applicatieprofiel.**

    -   Personen die bv. in een rusthuis wonen vormen een gezin op zichzelf en hebben een waarde voor het attribuut 'woonvorm' van gezinsrelatie.

    -   Nieuw in het model zijn de associaties van een persoon met een 'jurisdictie'. Deze associaties zijn 'inwonerschap' en 'staatsburgerschap'.

        -   Staatsburgerschap slaat op de rechten en plichten die een persoon heeft ten aanzien van een bepaalde jurisdictie (bijvoorbeeld het Koninkrijk België). Dit staat los van het gegeven of een persoon al dan niet inwoner is van de jurisdictie.

        -   De subtypes (subklassen) van de associatie klasse 'Staatsburgerschap' zijn te enten op de registers: Staatsburger = bevolkingsregister, Vreemdeling = vreemdelingenregister en BIS-register

        -   Inwonerschap wordt bepaald voor mensen die fysiek verblijven (met andere woorden, er hun hoofdverblijfplaats hebben) in een bepaalde jurisdictie.

        -   Als voorbeeld wordt gesteld: een Fransman die in Frankrijk woont en in België werkt heeft géén relatie 'inwonerschap' met de jurisdictie België. Indien zijn adres gemodelleerd wordt is dit een inwonerschap relatie met de jurisdictie Frankrijk, waaraan een verblijfsobject (gelegen in Frankrijk) kan gekoppeld zijn.

    -   Inwonerschap heeft associaties met verblijfplaatsen en de administratief beheerder (gemeente of consulaire post). Een 'verblijfplaats' is verder te specialiseren in onder meer 'Domicilie', 'Wettelijk Verblijf' en 'Verklaard Verblijf'. Deze verblijfplaatsen kunnen dan weer gekoppeld worden aan een 'Verblijfsobject', wat een gebouweenheid, ligplaats of standplaats voorstelt. Dit is niet meteen noodzakelijk voor 'U en Uw Gezin' maar waarschijnlijk wel nodig voor 'Uw Woonst en Patrimonium'.

-   De punten in de actielijst worden overlopen samen met het voorgestelde UML model voor Burgerloket Persoon, wat een extensie is bovenop het OSLO² Persoonsmodel.

    -   UUG4: extra voorgestelde attributen worden geïmplementeerd op 'Vreemdeling' klasse in OSLO².

    -   UUG25: adreswijzigingen worden gemapped op OSLO² 'heeftToekomstigBeheerder' mits toevoeging van associatieklassen met attributen voor adres (vrij tekstveld) en datum van aangifte.

    -   UUG28: bewijsstuk geboorte wordt mee opgenomen als extra attribuut van de klasse 'Geboorte' met code tabel op basis van rijksregister. Later wordt geëvalueerd of deze effectief getoond worden in het Burgerloket.

    -   UUG29: Implementeren als een relatie tussen twee personen (heeftRelatieMet - type Voogdij) en attribuut voor 'juridisch statuut' op niveau van de persoon die vertegenwoordigd wordt. **-\> Bespreken met Geert om voogdij te veranderen naar bewindvoering op basis van advies rijksregister.**

    -   UUG31: voor 'tijdelijke afwezigheid' wordt als extensie een datatype toegevoegd met attributen: datum, type, plaats

    -   UUG32: attributen codeRegister en omscrijvingRegister worden toegevoegd aan de klasse 'Staatsburgerschap'. Daarnaast is register ook een soort van 'bron' voor de gegevens. Dit concept komt ook nog in andere domeinen voor. -\> Nagaan met OSLO² team of er nood is om bij OSLO² Generiek het concept van Object heeft Bron toe te voegen (eventueel op basis van de [Provenance Ontology](https://www.w3.org/TR/prov-o/)).

    -   UUG33: domicilie en hoofdverblijfsplaats worden door elkaar gebruikt in rijksregister. **-\> Nagaan of OSLO² een manier heeft om om te gaan met synoniemen (bijvoorbeeld gebruik maken van alternatieve labels).**

    -   UUG34: in vebrand met overlijden wordt binnen een paar weken nagegaan wat er precies nodig is. Momenteel volstaat het om de attributen van OSLO² over te nemen.

    -   UUG35: Partner die vervat zit in element \'BurgerlijkeStaat\' tonen als de Huwelijkspartner.\ + Deze mappen met Huwelijk in OSLO² Persoon.

-   Het uitgewerkte [JSON-LD voorbeeld](https://drive.google.com/open?id=0B3DdQTFc4B-VbVBualYtQzhXMFU) kan gevisualiseerd worden met behulp van de online tool [http://json-ld.org/playground/](http://json-ld.org/playground/)

Besluit en acties
=================

1.  Alle voorstellen rond de openstaande punten in de actielijst werden aanvaard.

2.  De werkgroep evalueert de mapping uiterlijk tegen 29/03/2017.

3.  Jens werkt extra ondersteunende JSON-LD voorbeelden uit tegen 31/03/2017.

4.  Jens en Michiel bespreken feedback met het OSLO² team.

5.  Na het afwerken van voorgaande acties zorgen Jens en Michiel voor de nodige documentatie (@context voor Persoon en een specificatiedocument voor het Burgerloket Persoon applicatie profiel).
