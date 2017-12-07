**Informatie Vlaanderen**

Werkgroep OSLO² en "Meld Een Fout"

Datum: 15/02/2017 -- 14:30 -- 16:00

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Goedele Van der Spiegel, Carolien Willen, Jurgen Dooms,
Michiel De Keyzer, Nikolaos Loutas, Jens Scheerlinck

Verslaggever: Jens Scheerlinck

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Een eerste werksessie in Gent rond \"Meld Een Fout" met als doel het
uitklaren van onduidelijkheden en waar mogelijk al deels aligneren van
verschillen met bestaande standaarden.

Verloop
=======

-   Agenda

1.  Bespreken UML model en toelichten van (voorgestelde) wijzigingen t.o.v. synthesenota;

2.  Vergelijking informatiebehoefte/model voor (terug)melding met bestaande standaarden;

3.  Bespreken van de voorstellen, vragen en acties.

1.  **Bespreken UML model en toelichten van (voorgestelde) wijzigingen t.o.v. synthesenota**

2.  **Vergelijking informatiebehoefte/model voor (terug)melding met bestaande standaarden;**

-   Enkele relevante internationale standaarden werden geïdentificeerd:

    -   Klasse \"Melding\" en zijn relaties kan voor een groot deel gealigneerd worden met de \"Web Annotation Vocabulary\" (W3C Proposed Recommendation): [https://www.w3.org/TR/annotation-vocab/](https://www.w3.org/TR/annotation-vocab/)

    -   Specifiek voor het concept van \"terugmeldingen\" lijkt ook de Data Quality Vocabulary (W3C Working Group Note) interessant: [https://www.w3.org/TR/vocab-dqv/](https://www.w3.org/TR/vocab-dqv/)

    -   Daarnaast is de "Activity Vocabulary" (W3C Candidate Recommendation) interessant voor het modelleren van objecten en input/output relaties: [https://www.w3.org/TR/activitystreams-vocabulary/](https://www.w3.org/TR/activitystreams-vocabulary/)

3.  **Bespreken van de voorstellen, vragen en acties** [https://docs.google.com/spreadsheets/d/1sBvSuXdiqJxNBX1\_TU4oXGlybuM9bG3JON6kV23XpiI/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1sBvSuXdiqJxNBX1_TU4oXGlybuM9bG3JON6kV23XpiI/edit?usp=sharing)

-   Heeft een melding een titel nodig naast omschrijving?

    -   Titel als vrij tekstveld in te vullen door de indiener -\> blijft behouden.

-   Geometrie komt niet overeen met die van OSLO².

    -   Toevoegen van attributen 'wkt' en 'xmlGeometry' in datamodel voor de Generieke Terugmeldfaciliteit.

    -   'TypeGeometrie' hernoemen naar 'geometrieType' om terminologie te aligneren met OSLO².

    -   Behouden van extra attributen 'geometrieID' en 'beschrijving' om eventuele use case toe te laten waarbij geometrie op zich wordt uitgewisseld.

    -   Nagaan in welke mate OSLO en INSPIRE gealigneerd zijn met GeoJSON

-   Wat is de beoogde functionaliteit van het veld \"URI\"?

    -   Doorverwijzing waar externen informatie kunnen ophalen met betrekking tot deze melding.

    -   Kan potentieel gebruikt worden als unieke ID voor melding (indien stabiel) -\ verder te onderzoeken (wat wordt de base URI voor de meldingsfaciliteit?)

    -   Te beschouwen als de URL in een REST API voor deze melding.

-   Uitklaren van de begrippen "Indiener" en "Melderrol"

    -   Potentieel gebruik van Agent - te onderzoeken of Agent ook contactinfo omvat of enkel de subklassen ervan.

    -   MelderRol kan als codelijst worden opgenomen.

-   Klassen 'Status' en 'Historiek' kunnen worden samengevoegd in één enkele klasse.

-   Noodzaak en betekenis van aparte klasse voor 'Dossier'

    -   \"Melding" kan trigger zijn om een dossier aan te maken.

    -   Of, een dossier kan een trigger zijn om een melding te genereren.

    -   Het datamodel moet beide use cases toelaten -\ verder vergelijken van definities object, bijlage, etc.

-   Is het concept "ClusterMelding" nodig binnen het datamodel of kan dit vervat zitten in de applicatie logica?

    -   Goedele en Carolien werken use cases uit rond ClusterMelding.

-   Kan een codelijst gebruikt worden om "MeldingsEntiteit" te capteren?

    -   Omvat zowel organisaties als applicaties. Voor organisaties bestaat "Wegwijs" als codelijst, voor applicaties bestaat dit vandaag niet.

    -   Te bekijken hoe het concept van "kanaal" uit het OSLO² dienstverleningsmodel eventueel kan hergebruikt worden.

-   Hoe modelleren van de relatie tussen melding en object?

    -   Momenteel heeft 1 melding 1 meldingsobject aangezien elk meldingsobject kan toegewezen worden aan een andere organisatie of beheerder.

    -   Clusters zijn nodig om toe te laten 1 notificatie te versturen voor meerdere meldingen naar de indiener.

    -   Alternatief is om 1 melding meerdere meldingsobjecten te laten hebben en het concept object te abstraheren om ook 'dossier', 'geometrie' en 'bijlage' te omvatten.

    -   Jens en Michiel onderzoeken hoe dit kan gemodelleerd worden in lijn met de geïdentificeerde internationale standaarden.

Besluit en acties
=================

1.  Jens gaat definities toevoegen aan mapping
    spreadsheet.

2.  Jens en Michiel onderzoeken verder hoe
    Agent kan gebruikt worden voor "Indiener", hoe de vereiste
    functionaliteit met betrekking tot "Dossier" kan verwerkt worden in
    het data model, of "kanaal" kan gebruikt worden voor het concept van
    "MeldingsEntiteit" en hoe "objecten/meldingsobjecten" kunnen
    gemodelleerd worden in lijn met internationale standaarden.

3.  Goedele en Carolien werken uses cases uit
    rond "cluster meldingen".

4.  Tweede werkgroep vastgelegd op woensdag 08/03, 13:00 - 14:30
