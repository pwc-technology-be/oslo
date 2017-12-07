**Informatie Vlaanderen**

Werkgroep OSLO² en "Meld Een Fout"

Datum: 15/02/2017 -- 14:30 -- 16:00

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Goedele Van der Spiegel, Carolien Willen, Michiel De Keyzer,
Jens Scheerlinck

Verontschuldigd: Jurgen Dooms, Nikolaos Loutas

Verslaggever: Jens Scheerlinck

Bijlagen: [use cases rond
melding](https://drive.google.com/open?id=0B3DdQTFc4B-VQ1ZOR21yNE10Znc)
(nota Goedele Van der Spiegel)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Ter voorbereiding van deze werkgroep werd materiaal voorbereid op basis
van de input die tijdens de eerste werkgroep werd gegeven en de daaruit
voortvloeiende acties:

1.  [Een update van de mapping tussen het model dat werd voorgesteld in de GTMF synthesenota en internationale standaarden](https://docs.google.com/spreadsheets/d/1SJSe_JdWHia7XcipoWRwyVtfolZ7Vt-9futzR59Uobw/edit?usp=sharing). Ook de definities werden toegevoegd uit de verschillende vocabularia waar op gemapt wordt. Daarnaast is de \"Web Annotation Vocabulary\" intussen aanvaard als volwaardige W3C Recommendation, wat betekent dat ze aanvaard is door de brede community en bijgevolg stabiel.

2.  [Een up-to-date actielijst](https://docs.google.com/spreadsheets/d/1ol-KHZSkwmiwZVU166074YOj5XfojHUkbSx-Hi0DgPg/edit?usp=sharing), welke we zullen gebruiken als leidraad voor de werkgroep. Voeg hier indien gewenst gerust vragen en opmerkingen aan toe.

3.  [Nieuwe versie van het voorgestelde UML diagram](https://drive.google.com/open?id=0B3DdQTFc4B-VUEh2WVVRNElKVm8) op basis van de internationale standaarden.

4.  [Een object diagram](https://drive.google.com/open?id=0B3DdQTFc4B-VWlFHVW5VZUI0SUU), dat op basis van het UML model een specifieke instantiatie weergeeft.

5.  Op basis van het object diagram hebben we ook reeds [een voorbeeld JSON(-LD) bestand](https://drive.google.com/file/d/0B3DdQTFc4B-VWE43eXROdzBGT1E/view) gecreëerd. Dit bestand is makkelijker te bekijken en evalueren in een online editor: [http://www.jsoneditoronline.org/?id=29ea40f93fe7bc74941f172c871c0e4c](http://www.jsoneditoronline.org/?id=29ea40f93fe7bc74941f172c871c0e4c)

Agendapunten:

1.  Bespreken van het bovenstaand materiaal op basis van de actielijst;

2.  Doorlopen van de mapping om definities te valideren.

3.  Toetsen van het voorgesteld model aan de verschillende use cases;

4.  Bepalen van volgende stappen.

Verloop
=======

-   Het voorgestelde model werd besproken en de volgende feedback werd vergaard:

    -   Voor wat betreft het concept van Status of Historiek is het nodig om te kunnen linken met een specifieke agent binnen een organisatie die de statuswijziging heeft doorgevoerd. Dit concept en de use cases zijn analoog aan 'dossierbeheerder' in DOSIS.

    -   Voor wat betreft de link tussen een MeldingsObject, Organisatie die de melding toegewezen krijgt en Dataset is het mogelijk dat hier nog een stap tussen zit. Bv. Geopunt die een bepaalde melding valideert vooraleer deze wordt doorgestuurd aan de afhandelaar (bij LED zelfde principe). PwC bekijkt of toevoegen van dcat:catalog en publisher van catalog deze use case kan dekken.

    -   Op basis van de use cases die werden uitgewerkt door Goedele werd de nood besproken om ook een status te kunnen bepalen op niveau van 'Object'. Minstens status, datum en omschrijving zijn nodig als attributen.

    -   Er werd beslist de 'meldingsEntiteit' op te splitsen in een organisatie en een applicatie.

-   Met behulp van het object diagram werd de toepasbaarheid van het model op de verschillende use cases besproken:

    -   Om binnen een melding bepaalde gerelateerde objecten te kunnen doorsturen naar bepaalde afhandelaars is het nodig om de individuele objecten met elkaar te kunnen linken. Wanneer, zoals nu, de objecten enkel gelinkt zijn aan de melding maar niet met elkaar is het niet mogelijk om te gaan bepalen wat samenhangt en wie wat mag zien in de verdere afhandeling. Voor het model zal bekeken worden of een zelf relatie tussen objecten deze use case kan dekken.

    -   Het attribuut 'bijlage' van een object kan omgedoopt worden tot 'additioneleInformatie' om naast effectieve bijlagen ook meer generieke URLs toe te laten.

Besluit en acties
=================

1.  Volgende werkgroep zal plaatsvinden op 28/03/2017, 13:30

2.  PwC zal het data model verder uitwerken op basis van de ontvangen input. Daarnaast zullen een aantal verschillende object diagrammen en JSON-LD voorbeelden worden uitgewerkt om de verschillende use cases te toetsen.

3.  Tegen volgende werkgroep nemen Goedele en Carolien de mapping door samen met de definities en geven hun feedback.

4.  Vervolgens zullen definities en labels vertaald worden naar het Nederlands.
