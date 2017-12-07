**Informatie Vlaanderen**

Werkgroep Informatiemodel - Toestemming - Contactvoorkeuren

Datum: 06/09/2017 -- 10:00 -- 12:00

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Goedele Van der Spiegel, Niko Tanghe, Kristof De Causemaeker,
Dries Beheydt, Michiel De Keyzer, Jens Scheerlinck

Verontschuldigd: David Van Den Brande, Annelies De Craene, Philip
Boivin, Omaar Verack

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Nieuwe versie van het](https://drive.google.com/open?id=0B3DdQTFc4B-VQTM4NnJFZUdVQkE) informatiemodel o.b.v. feedback overleg

-   [Actielijst](https://drive.google.com/open?id=1muvFEysP6UNGWGoe2BkoL7aqiUAZk5QwOa4vaElpsqs)

-   Mapping technische analyse - draft informatiemodel

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

-   Bespreken van eerste draft informatiemodel voor toestemming - contactvoorkeuren.

-   Feedback capteren op functioneel vlak en van ontwikkelaars.

Verloop
=======

-   Context

    -   De eerste draft versie van het informatiemodel voor toestemming - contactvoorkeuren is gebaseerd op concepten uit volgende bronnen:

        -   [W3C Working Draft - Permissions API](https://www.w3.org/TR/permissions/)

        -   [GDPR wetgeving](http://www.eugdpr.org/)

    -   Contactvoorkeur is opgevat als een specialisatie (subklasse) van Toestemming.

    -   In tegenstelling tot andere domeinen in het kader van Burgerloket bestaat voor de use case rond contactvoorkeuren geen eenduidig referentiemodel op niveau van OSLO, ISA of W3C.

    -   Het draft informatiemodel werd getoetst aan de [aanzet van David Van Den Brande op Confluence](https://vlaamseoverheid.atlassian.net/wiki/spaces/BLAR/pages/76758321/Notifications#Notifications-LogicalDataModel-Consent(eenaanzet)) en de [Technische analyse Contactvoorkeuren.](https://vlaamseoverheid.atlassian.net/wiki/spaces/BN/pages/78418862/Technische+analyse+Contactvoorkeuren)

    -   Het werd opgesteld met als vertrekpunt dat het ook bruikbaar moet zijn voor toestemming (consent) die niet gerelateerd zijn aan contactvoorkeuren.

    -   Nieuwe begrippen die geïntroduceerd werden in het informatiemodel zijn:

        -   **Toestemming** = een specifieke toestemming gegeven door een specifieke Agent. Dit is de klasse die in praktijk wordt aangeroepen om te kijken of iemand toestemming/consent gegeven heeft.

        -   **ToestemmingDescriptor** = omschrijving van de toestemming door een Agentschap. Omvat o.a. consent vraag, databron (systeem, overgenomen uit technische analayse contactvoorkeur), data controller (verantwoordelijke voor beheer van de data) en data processor (organisatie of systeem die de data gebruikt, bv. voor versturen notificatie).

        -   **Contactvoorkeur(Descriptor)**, subklassen van Toestemming(Descriptor) waar specifiek de contactinformatie in wordt bijgehouden.

-   Feedback op draft informatiemodel

    -   Voor contactvoorkeuren moeten gebruikers ook de mogelijkheid krijgen om naast kanaal, frequentie, email en telefoon ook te bepalen voor welke notificatie categorie (codelijst uit Notificatiecomponent) ze notificaties wensen te ontvangen. Dit zal worden toegevoegd aan de klasse "**Contactvoorkeur**".

    -   Functioneel zullen gebruikers toestemming kunnen geven op Burgerloket niveau (voor alle aangesloten partners). Achterliggend zal per partner een aparte record worden aangemaakt, zodat deze toestemmingen achteraf individueel te beheren zijn.

    -   De toestemming voor het bijhouden en gebruiken van een e-mail adres en telefoonnummer zullen opgeslagen worden als aparte toestemmingen. Een constraint dient toegevoegd te worden aan de klasse "**Contactvoorkeur**", waarbij per instantie een telefoonnummer of een e-mail adres wordt opgeslagen, maar niet beiden.

    -   Het attribuut "**consentvraag**" van de klasse "**ToestemmingDescriptor**" is mogelijks hetzelfde voor heel Burgerloket. Het is aangewezen om dit attribuut te koppelen aan een codelijst met apart beheer.

    -   Het attribuut **dataController** verwijst naar de beheerder van de informatie. Dit komt overeen met het concept van eigenaar in de technische analyse contactvoorkeuren, alleen moet volgens GDPR deze eigenaar expliciet worden geïdentificeerd. Dit kan gebeuren op basis van de Wegwijs ID.

    -   Het attribuut **dataProcessor** verwijst naar de organisatie(s) die de informatie gebruiken. Bv. Informatie Vlaanderen voor het versturen van notificaties via de Notificatiecomponent of het bijhouden van dossierstatussen in DOSIS.

    -   In het draft informatiemodel is een expliciete link tussen de klasse "Toestemming" en een "Agent" opgenomen, waarbij verwacht wordt dat deze Agent te identificeren is a.d.h.v. een rijksregister- of ondernemingsnummer. De werkgroep dient na te gaan of dit eventueel problemen oplevert in de context van ondernemingen waarbij machtigingen gegeven worden of in de context van voogdij.

-   Overlopen [actielijst](https://drive.google.com/open?id=1gXNUuBvJnSLj52juTIbd5JFaJ-v3K-OwHGFG68KYZ6w):

    -   **T2**: Agentschappen gaan de keuze hebben (zie technische analyse). In uitwerken voorbeelden hiermee rekening houden.

    -   **T3**: Right to be forgotten: te onderzoeken wat impact is op Burgerloket. Welke informatie kan verwijderd worden? Document (webpagina) nodig dat zegt wat dit betekent en wat je toch nog te zien krijgt op decretale basis.

    -   **T6**: Notificatie kanaal en frequentie mee op te nemen in model.

    -   **T7**: dataProcessor wordt steeds gelinkt aan een Organisatie.

    -   **T8**: Zaken als toestemming i.f.v. de mobiele applicatie voor Burgerloket, bv. locatie, camera, contacten,... zullen gewoon op Operating System niveau (iOS/Android/Windows Phone) worden bijgehouden, niet in de backend van Burgerloket/Contactvoorkeuren. Wel af te stemmen met front end team of zij "toestemming" voor andere zaken nodig hebben, bv. cookies.

    -   **T9**: Contactvoorkeuren en toestemming blijven altijd samen opgeslagen. Ofwel bij Contactvoorkeuren component ofwel bij agentschap/partner.

Besluit en acties
=================

1.  Jens en Michiel raadplegen jurist i.f.v. vereisten GDPR en privacywetgeving (**deadline: 22/09/2017**).

2.  Jens update model o.b.v. feedback, werkt documentatie uit inclusief voorbeelden (**deadline: 14/09/2017**) .

3.  Jens en Michiel stemmen model af met Katrien Mostaert i.f.v. noden en use cases front end (**deadline: 22/09/2017**).
