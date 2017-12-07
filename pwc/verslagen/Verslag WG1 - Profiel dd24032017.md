**Informatie Vlaanderen**

Werkgroep OSLO² en "Profiel"

Datum: 24/03/2017 -- 13:00 -- 14:30

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

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Een eerste werksessie rond het Burgerloket \"Profiel" met als doel het
uitklaren van onduidelijkheden in de informatieanalyse en waar mogelijk
al deels aligneren van verschillen met OSLO² en bestaande internationale
standaarden.

Agenda:

1.  Inleiding door Michiel en Jens m.b.t. het doel van deze werkgroep en het beoogde eindresultaat.

2.  Bespreken van de vragen en voorstellen in de actielijst.

3.  Bespreken van mapping en het voorgesteld UML model.

Verloop
=======

-   Jens en Michiel stellen een model voor waarbij voor het concept profiel wordt gesteund op de [FOAF vocabulary](http://xmlns.com/foaf/spec/), waar profiel gedefinieerd wordt als een "PersonalProfileDocument" met als "primary topic" de persoon die door het profiel wordt beschreven.

-   Voor de beschrijving van de persoonsgegevens kan gesteund worden op het OSLO² vocabularium voor "Persoon". Dit vocabularium bevat naast algemene persoonskenmerken ook het concept "GeregistreerdPersoon" met een officiële identificator (het INSZ nummer). Dit kan hergebruikt worden om het onderscheid te maken op termijn tussen personen die zwak vs sterk zijn geauthenticeerd.

-   Ook op basis van de [FOAF vocabulary](http://xmlns.com/foaf/spec/) werd een extensie toegevoegd aan de klasse "Persoon" voor het concept van een "OnlineAccount", bv. een account die kan gebruikt worden om in te loggen op een profiel.

-   De volgende punten uit de actielijst werden besproken:

    -   PR1 - Zijn er andere relaties tussen burgers nodig dan deze die in scope zitten van U en Uw Gezin?

        -   Geen andere relaties nodig in-scope van profiel.

    -   PR2 - Aligneren met OSLO² Persoon.

        -   Voorstel om OSLO² Persoon te gebruiken om een persoon te beschrijven werd aanvaard door de werkgroep.

    -   PR3 - Authorisatie gegevens

        -   ACM houdt zich bezig met deze informatie en het zit niet vervat in het profiel.

    -   PR4- Hergebruik bestaande vocabularia

        -   Verder onderzoeken van de FOAF vocabulary.

    -   PR5 - Contactvoorkeuren

        -   Deze moeten worden gemodelleerd binnen het domein van notificatie. De notificatie bouwsteen zal zich bezighouden met het opslaan van de contactvoorkeuren van de Burger per kanaal en per aangesloten dienst. Deze notificatie bouwsteen zal wel als "default" gegevens de contactgegevens zoals e-mail adres en telefoonnummer kunnen ophalen uit het profiel. Daarom volstaat het om in het model voor profiel een associatie op te nemen naar een externe klasse contactvoorkeuren (dewelke dan verder uitgewerkt wordt binnen het notificatie traject).

    -   PR6- INSZ als identificator voor de persoon die beschreven wordt door het profiel?

        -   Te bespreken met David of Nathalie wat de implicaties hiervan zijn. Welke machtigingen zijn nodig etc?

    -   PR7 - Domicilie adres en verzendadres

        -   Voorlopig geen use cases hiervoor. Generiek adres kan mee opgenomen worden in model voor gebruik in de toekomst.

    -   PR8 - Koppelingen tussen profielen

        -   PwC werkt een aantal voorbeelden uit om te kijken hoe dit werkt volgens het huidig voorgestelde model.

    -   PR9 en PR10 met betrekking tot thema's

        -   Voorlopig on hold

    -   PR11 attribuut "taal"

        -   Hiermee wordt de taal van de persoon bedoelt. Dit zal in eerste instantie altijd 'NL' zijn.

    -   PR14 in verband met profielen voor organisaties:

        -   Zit buiten de scope van het Burgerloket profiel, maar geen probleem als het mogelijk is in het model door profiel op niveau van 'Agent' te modelleren.

-   Daarnaast werden de volgende vragen geopperd:

    -   Is het nodig een link te voorzien tussen de klassen PersonalProfileDocument en OnlineAccount om te kunnen duiden welke account kan gebruikt worden om in te loggen bij welk profiel? -\> Dit zal getoetst worden aan de hand van de uit te werken voorbeelden.

    -   Is het nodig om op niveau van profiel een status te kunnen meegeven of is dit eerder interne keuken?

-   Tot slot werd de mapping tussen de informatieanalyse van profiel en de standaarden OSLO² en FOAF overlopen. Bemerkingen werden rechtstreeks in het document achtergelaten.

Besluit en acties
=================

1.  Jens werkt voorbeelden uit in JSON-LD om
    het model te staven, deze worden voorgesteld tijdens een tweede
    overleg rond Profiel.

2.  Philip duid aan welke velden (mogelijks in
    de toekomst) in scope zitten van het profiel in de spreadsheet met
    de informatieanalyse.

3.  Een Doodle wordt uitgestuurd om een datum
    vast te pinnen voor een tweede werkgroep.
