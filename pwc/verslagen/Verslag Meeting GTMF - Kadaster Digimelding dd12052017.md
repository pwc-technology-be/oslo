**Informatie Vlaanderen**

Uitwisselen van gedachten rond meldingsfaciliteit

Datum: 12/05/2017 -- 15:00 -- 16:00

Locatie: Conference call

Aanwezig: Goedele Van der Spiegel, Carolien Willen, Michiel De Keyzer,
Jens Scheerlinck, [Jaap-Willem
Sjoukema](mailto:Jaap-Willem.Sjoukema@kadaster.nl),
[Monique Schaafsma](mailto:Monique.Schaafsma@kadaster.nl)

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [API documentatie indienen terugmelding mei 2017](https://drive.google.com/open?id=0B3DdQTFc4B-VcUFRRFB4OUdfZjA)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

Het doel van deze meeting was om ideeën en ervaring uit te wisselen rond
het bouwen van een (terug)meldingsfaciliteit. Met mensen van het PDOK in
Nederland, welke al een operationele versie van een generieke
meldingsfaciliteit op geografische basisregistraties hebben.

Verloop
=======

-   Jaap-Willem geeft aan dat de gevolgde benadering voor het meldingssysteem van PDOK is om zo min mogelijk informatievelden verplicht te maken bij het aanmaken van een melding en waar mogelijk informatie automatisch te laten invullen door de applicatie.

-   Voorlopig wordt enkel aan de slag gegaan met geografische meldingen. Hiervoor werd gealigneerd met de GeoJSON standaard.

-   Een voorbeeld van een integratie in een web applicatie is te vinden op: [verbeterdekaart.nl](http://verbeterdekaart.nl)

-   Voor andere aspecten van het model werd niet gekeken naar bestaande standaarden, maar vertrokken van de nodige functionaliteit.

-   De bedoeling is om op termijn ook niet-geografische melding toe te laten in het systeem.

-   Momenteel loopt er een project om de melding API ook beschikbaar te maken voor externe organisaties. Diet zou eventueel toelaten om ook meerdere meldingen in bulk aan te maken.

-   Huidige gebruikers bestaan uit zowel particulieren als bedrijven en publieke organisaties. Statistieken worden hieromtrent bijgehouden op basis van analyse van de e-mailadressen (voor het aanmaken van een melding is geen authenticatie nodig).

-   Het datamodel van het basisregister zit geconfigureerd achter de webapplicatie waar de melding wordt in aangemaakt.

-   Op het vlak van identifiers:

    -   Voor elke melding wordt automatisch een nieuw nummer gegenereerd van X aantal karakters. Na verloop van tijd is het mogelijk dat de nummers 'op' zijn en dat de nummering opnieuw moet beginnen. Dit kan eventueel opgelost worden door het toevoegen van een prefix met het jaartal.

    -   Na een paar maanden worden meldingen gearchiveerd.

    -   Wettelijk moet de informatie minstens 5 jaar bewaard worden

-   Rond het groeperen/clusteren van meldingen, het toelaten van meldingen met meerdere objecten zijn voorlopig nog geen use cases, maar die zullen er hoogstwaarschijnlijk wel aankomen met het openstellen van de API. Dit kan potentieel ook problematisch worden voor het afhandelen en communiceren rond meldingen.

    -   Een mogelijke oplossing waar aan gedacht werd was om voor deze meldingen de notificaties te groeperen en gebundeld te versturen in één enkele e-mail (een soort van daily of weekly digest, red.)

-   Rond het topic van rollenbeheer bestaan momenteel enkel melder en bronhouder. Echter verwachten zij binnenkort ook geconfronteerd te worden met use cases waarbij extra rollen zoals validator opduiken.

-   Voor wat betreft meldingen op niet bestaande objecten worden x,y coördinaten meegegeven plus een beschrijving. Echter, het al dan niet bestaan van objecten is mede afhankelijk van de gebruikte applicatie. Bv. verbeterdekaart.nl is gebaseerd op een Web Map Tile Service (WMTS).

-   Voor bestaande objecten wordt de identifier van het object meegestuurd samen met de attributen die de melder heeft aangeduid als zijnde foutief. De melding wordt doorgestuurd naar de bronhouder, die op zijn beurt de melding kan doorverwijzen naar een andere bronhouder.

Besluit en acties
=================

1.  PwC vergelijkt datamodel van PDOK met huidig model voor (terug)meldingen.

2.  Naar toekomst toe wordt contact onderhouden om gedachten en ervaring uit te wisselen.

3.  PwC vraagt slides op m.b.t. gebruikersstatistieken.
