**Informatie Vlaanderen**

Werkgroep OSLO² Persoon en Burgerloket U en Uw Gezin & Profiel

Datum: 25/01/17 -- 11:00 -- 13:30

Locatie: [Boudewijngebouw
Brussel](https://www.google.be/maps/place/Boudewijngebouw/@50.8567731,4.3526172,17z/data=!3m1!4b1!4m5!3m4!1s0x47c3c38369503633:0xe176454918e1b130!8m2!3d50.8567731!4d4.3548059?hl=nl)

Aanwezig: An Boes, Bruno De Vrieze, Philip Boivin, Valère Bouserie,
Michiel De Keyzer, Jens Scheerlinck

Verontschuldigd: Katrien Desmet, Annelies De Craene, Dries Beheydt, Raf
Buyle

Verslaggever: Jens Scheerlinck

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Een eerste werksessie in Brussel rond \"U en Uw Gezin\" en \"Profiel\"
in relatie met OSLO² (Persoon) met als doel het uitklaren van
onduidelijkheden en waar mogelijk al deels aligneren van verschillen.

Verloop
=======

-   Agenda
    1. Updates in analyse \"U en Uw Gezin\", Analyse \"Profiel\" en status \"OSLO² Persoon\";
    2. Vergelijking informatiebehoefte/model \"U en Uw Gezin\" en \"Profiel\" met OSLO² Persoon: inleiding draft mapping en draft UML model
    3. Bespreken van de voorstellen, vragen en acties

- Updates sinds initieel overleg 25/01/2017

    -   Persoon

        -   Mapping MAGDA -- OSLO<sup>1</sup> en relevante documentatie hieromtrent is te vinden op [Google Drive](https://drive.google.com/drive/folders/0B5lYzh34rTaueTNQaEZVanJSNEE).

        -   Documenten 'DraftOSLO2Persoon' en 'Evaluatie OSLO tov MAGDA' interessant om door te nemen.

        -   Recentste versie van 'U en Uw Gezin' informatiemodel te vinden op de [Confluence](https://vlaamseoverheid.atlassian.net/wiki/display/BLWWOOM/A.+Informatiemodel). Wijzigingen bevatten onder meer: verwijderen attribuut arbeidskaart en toevoegen van concept register.

-   Vergelijking informatiebehoefte/model \"U en Uw Gezin\" en \"Profiel\" met OSLO² Persoon: inleiding draft mapping en draft UML model

    -   Voorstelling door Michiel De Keyzer van de eerste analyse en draft voorstellen van PwC:

        -   [Draft mapping tussen de informatiebehoeften van \"U en Uw Gezin\" en OSLO² (voornamelijk Persoon)](https://docs.google.com/spreadsheets/d/1WMZhT5OjQDDiU08RthLOG6nV7ydPRGQ0RPu9SeffO9E/edit?usp=sharing);

        -   [Draft UML model voor 'U en Uw Gezin'](https://drive.google.com/file/d/0B8SEyUR0B9eQS3NManBEazZFb00/view?usp=sharing);

        -   [Voorstellen, vragen en acties](https://docs.google.com/spreadsheets/d/1sBvSuXdiqJxNBX1_TU4oXGlybuM9bG3JON6kV23XpiI/edit?usp=sharing).

-   Bespreken van de voorstellen, vragen en acties

1.  **Wat te verstaan onder geregistreerd persoon?**

    -   Voorstel om geregistreerd persoon te definiëren als persoon met een INSZ.

        Als registers -\> basisregisters personen.

        Er bestaat echter een kleine kans dat mensen niet in één van deze registers vallen. Onderwijs heeft bv. specifieke nummers in omloop waar personen aan gekoppeld kunnen worden. Het (data) model moet idealiter hier ook bruikbaar voor zijn.

    -   Klasse 'Persoon' -\> attribuut 'identificator' (kan alles zijn)

        Klasse 'Geregistreerd persoon' -\> in één van de basisregisters (met INSZ)

    -   Case als voorbeeld: buitenlander die in België komt werken maar niet woont is enkel ingeschreven in BIS register en heeft geen eID (maar hebben wel een INSZ).

    -   Welke identiteitsbewijzen mogelijk gecapteerd moeten worden binnen model, moet beslist worden door Bruno.

2.  **Concept afstamming**

    -   Afstamming in stijgende en dalende lijn nodig want andere attributen zijn eraan verbonden.

    -   In BL request in één call naar de API zowel ouders als kinderen zien (dit zijn ook twee wettelijke types in het RR geworden).

3.  **Concept gezin**

    -   Samenwonenden zijn gelinkt aan dezelfde referentiepersoon. In RR wordt dit gezien als gezin (zelfde domicilie).

    -   In BL is begrip gezin ruimer opgevat (ook met kinderen die niet meer samenwonen).

        Requirement in BL: 1 JSON call waarin alle gezinsleden opgevraagd worden

    -   In RR: bij gezinslid zie je enkel de referentiepersoon en bij opvragen referentiepersoon zie je enkel de gezinsleden. In BL wordt dit samengevoegd.

    -   Concept 'samenwonenden' is specifieker dan gezin (officieel samenwonend).

    -   **Consensus**: gezin op basis van referentiepersoon is een nuttig begrip. Maar aparte entiteit \"gezin\" bestaat niet als concept in RR. Dus link tussen 2 personen \"referentiepersoon\" zou voldoende zijn in OSLO.

4.  **Begrip 'gehuisvest door'**

    -   Heeft verband met kinderen met gescheiden ouders die naast hun domicilie adres ook het adres van de tweede ouder officieel willen registreren.

    -   Dit zou ook moeten weergegeven worden in BL (maar is nog niet het geval).

5.  **Relatie tussen vreemdeling (MAGDA) en concepten in OSLO² (inwoner, niet-inwoner...)**

    -   BL velden komen hoofdzakelijk uit het wachtregister

    -   \"RechtOpTerugkeer\" is geen wettelijk gegeven in het RR maar kan wel nuttig zijn voor gegevensuitwisseling.

    -   Concept 'inwoner' is momenteel verwarrend in OSLO: voor gemeentes zijn inwoners \"inwoners van de gemeente\".

    -   RR bestaat uit bevolkingsregister (BE nationaliteit), wachtregister en vreemdelingenregister (kortverblijf)

    -   Meer informatie over informatietypes in het rijksregister zijn te vinden op: [http://www.ibz.rrn.fgov.be/nl/rijksregister/reglementering/onderrichtingen/lijst-van-de-informatietypes/](http://www.ibz.rrn.fgov.be/nl/rijksregister/reglementering/onderrichtingen/lijst-van-de-informatietypes/)

6.  **Concept handicap**

    -   Aparte service GeefHandicap in MAGDA

    -   Nodig om dit binnen u en uw gezin te tonen? Of eerder gerelateerd aan zaken als werk, mobiliteit, rechten,...

    -   In MAGDA zit handicap bij het domein sociale zekerheid

    -   'PercentageOngeschiktHeid': na te kijken of definitie exact hetzelfde is bij kind en volwassene 

    -   **Consensus:** begrip voorlopig parkeren tot het duidelijker is waar dit moet komen (output van dienstverlening, als onderdeel van informatie omtrent gezondheidszorg)

7.  **KBI velden**

    -   Hierover wordt volgende week een meeting georganiseerd.

8.  **Adres**

    -   **Consensus**: relatie is nodig maar hoe het modelmatig wordt verwerkt is minder van belang voor BL. PwC gaat onderzoeken welke optie het best werkt.

    -   OSLO adres momenteel aan het werken rond gelijktrekken CRAB en BEST.

    -   Tony Vanderstraeten als relevant contactpersoon.

9.  **Echtgenoot/partner/huwelijk**

    -   Wanneer gehuwd, stopt automatisch het wettelijk samenwonen

    -   Wat betekend partner in andere landen? Dit moet worden geanalyseerd.

    -   **Consensus**: in datamodel BL nog niet samenvoegen partner/echtgenoot, dit zal worden gedaan door de front end logica. Beide relaties moeten afzonderlijk blijven bestaan in het datamodel 

10. **Nationaliteit(en)**

    -   Meerdere mogelijk + concept van \'verkregen op\' (dat geen historiek is) ontbreekt momenteel.

    -   In RR: hoofdnationaliteit en andere nationaliteiten. Gevolgen voor bv. Studietoelage (hier wordt gekeken naar hoofdnationaliteit).

    -   Daarnaast ook nog reden van verkrijgen (geboorte, adoptie, ...)

    -   Meer informatie te vinden in MAGDA documentatie.

11. PwC gaat voorbeeld JSON maken op basis van voorbeelden in documentatie MAGDA voor geef persoon en andere relevante services.

Besluit en acties
=================

1.  Bruno De Vrieze zal aangeven welke identiteitsbewijzen opgenomen
    moet worden in het model.

2.  Jens gaat voorbeeld JSON maken op basis van
    voorbeelden in documentatie MAGDA voor geef persoon en andere
    relevante services.

3.  An Boes kan XSD schema's bezorgen aan Jens en Michiel.

4.  Volgende meeting kan doorgaan om 22/02 10u in Brussel **-\> Done**

5.  Jens/Michiel stuurt link door naar 'FOAF' documentatie in verband
    met profiel **-\> Done**.

6.  Jens/Michiel verwerken de besproken punten in een nieuwe versie van
    het model, en nemen de zaken die nog moeten uitgeklaard (en
    eventueel aangepast) worden op met OSLO
