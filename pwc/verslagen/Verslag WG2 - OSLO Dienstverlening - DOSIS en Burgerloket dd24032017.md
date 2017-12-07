**Informatie Vlaanderen**

Werkgroep OSLO² Dienstverlening en Burgerloket DOSIS

Datum: 24/03/2017 -- 15:00 -- 16:50

Locatie: [VAC
Gent](https://www.google.be/maps/place/VAC+Gent/@51.0371235,3.7065649,17z/data=!3m1!4b1!4m5!3m4!1s0x47c37162c6c82103:0xad3dbba6a7c4cc90!8m2!3d51.0371201!4d3.7087536?hl=nl&dg=dbrw&newdg=1)

Aanwezig: Thomas Dhaenens, Bart Misseeuw, Goedele Van der Spiegel, Raf
Lauriks, Ziggy Vanlishout, Dries Beheydt, Michiel De Keyzer, Jens
Scheerlinck

Verontschuldigd: Katrien Mostaert, Nikolaos Loutas, Raf Buyle

Verslaggever: Jens Scheerlinck

Bijlagen:

-   [Mapping tussen DOSIS informatiemodel burgers en OSLO² Dienst](https://drive.google.com/open?id=12aKDZjPIgJoIlJ6v5rs2Uni1jw_yqu5wcS4MFUCWGEI)

-   [UML diagram voor het luik Dienstverlening/Lopende Zaken van Burgerloket](https://drive.google.com/open?id=0B3DdQTFc4B-VQXk5V1YxS2RiUkU) (versie voorgesteld tijdens werkgroep) en [aangepaste versie op basis van feedback werkgroep](https://drive.google.com/open?id=0B3DdQTFc4B-Vblp1RzE2UUtBV1U).

-   [JSON-LD voorbeeld](https://drive.google.com/open?id=0B3DdQTFc4B-VWWI4TTZ0VU5LdVU)

-   [Actielijst](https://docs.google.com/spreadsheets/d/1UeVfgAygXyE4Z0339XKrVjbqg1pMB1CHqkLiFK21ABk/edit?usp=sharing)

**////////////////////////////////////////////////////////////////////////////////////////////////////////**

Doelstelling
============

-   Voorstel van eerste model rond geïnstantieerde dienstverlening/transactie.

-   Behandelen van actiepunten voortvloeiend uit de initiële mapping.

-   Analyseren van impact op DOSIS/Burgerloket.

-   Bepalen van de volgende stappen.

Verloop
=======

-   De werkgroep bespreekt het voorgesteld model voor geïnstantieerde dienstverlening/transactie.

    -   Het introduceren van het concept transactie als een klasse in het model lijkt niet noodzakelijk. Alle extra elementen zoals status en bron kunnen rechtstreeks als extensie bovenop de klasse PubliekeDienstverlening gemodelleerd worden.

    -   Dit transactioneel model zit op een derde conceptueel niveau met betrekking tot dienstverlening:

        -   Niveau 1: IPDC catalogus op Vlaams niveau

        -   Niveau 2: catalogus van diensten op niveau van de steden en gemeenten, diensten die in praktijk kunnen afgenomen worden door burgers of organisaties. In sommige gevallen is het mogelijk dat er een 1 op 1 relatie bestaat met niveau 1.

        -   Niveau 3: de specifieke invulling van een dienstverlening zoals deze wordt afgenomen door een specifiek persoon of een specifieke organisatie op een bepaald tijdstip. Op dit niveau kunnen we spreken van transactionele dienstverlening ofwel het niveau "transactie".

    -   De klasse "StatusHistoriek" kan hernoemt worden naar "Status", echter, de klassen in dit (abstract) model hebben allen impliciet een historiek.

    -   De relatie tussen een dienstverlening en de uitvoerder "wordtUitgevoerdDoor" moet gedefinieerd worden tussen "PubliekeDienstverlening" en "Agent" i.p.v. "Organisatie".

    -   De "bron", zijnde het systeem dat de nodige informatie aanlevert aan DOSIS, wordt niet gelijkgesteld aan de OSLO² Dienst klasse "Kanaal". Gelijkaardige concepten bestaan bij, Persoon, Melding en Notificatie. Er wordt gekeken naar de Provenance Ontology om dit generiek te definiëren binnen OSLO².

    -   De "heeftPartcipatie" associatie met klasse "Partcipatie" zal voortvloeien uit de toegangsrechten in DOSIS. De rol die daaraan gekoppeld kan worden (bv. aanvrager of begunstigde) worden momenteel niet voorzien en zullen in de toekomst moeten worden opgenomen, bijvoorbeeld op basis van een code tabel. Dit vergt extra input van de aanleverende bronnen.

-   Met betrekking tot het aanmaken van unieke en persistente URIs bespreekt de werkgroep het volgende: voor een pragmatische implementatie om mee te beginnen kunnen de globaal unieke URIs (= IDs) voor de transactionele dienstverlening technisch gegenereerd worden binnen DOSIS door het samenvoegen van bronnummer en dossiernummer en conform de [URI standaard van de Vlaamse Overheid](https://drive.google.com/open?id=19QoC5qOiOa2o_rsL27YRmy-zw_nYWqe5pLuRSh2enMo). Deze functionaliteit wordt echter los van DOSIS geprofileerd.

-   Wat betreft de additionele attributen die binnen DOSIS aan een dossier worden gekoppeld, zoals "isVertrouwelijk", "isPubliek" en "isDeleted" zullen in dit model opgenomen worden als attributen van de klasse "Status".

-   Daarnaast wordt de reflectie gemaakt door de werkgroep of de use case rond transactionele dienstverlening ook moet gecapteerd worden binnen de specificatie van OSLO² dienstverlening.

-   Tot slot wordt de discussie gevoerd rond hoe in het burgerloket (en later andere domeinen) omgegaan moet worden met de output van dienstverlening.

    -   Concreet moet bepaald worden of en hoe in andere domeinen, zoals bv. "U en Uw Gezin", de link tussen bv. een identiteitsbewijs en de dienstverlening die dit identiteitsbewijs gegenereerd heeft als output moet worden gecapteerd.

    -   Daarnaast wordt de vraag geopperd wanneer de output onttrokken wordt aan de transactie (met andere woorden, niet langer zal getoond worden binnen Burgerloket 'Lopende Zaken') en op zichzelf staat als object.

    -   PwC analyseert hoe dit modelmatig kan verwerkt worden: output en bewijsstuk als subklassen van object (cfr. Core Evidence & Criterion Vocabulary) of met object die een hoedanigheid heeft in de rol van bewijs of output.

Besluit en acties
=================

1.  De besluiten en acties zijn samengevat in de
    [actielijst](https://docs.google.com/spreadsheets/d/1UeVfgAygXyE4Z0339XKrVjbqg1pMB1CHqkLiFK21ABk/edit?usp=sharing).

2.  Volgende Doodle is opgesteld om de
    volgende werkgroep in te plannen en dient ingevuld te worden
    uiterlijk op 29/03/2017: <http://doodle.com/poll/64zmcm7hanx4vfa3>

3.  Jens en Michiel verwerken de ontvangen
    feedback en stellen nieuwe versies van het materiaal ter beschikking
    van de werkgroep uiterlijk op 31/03/2017.
