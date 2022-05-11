---
layout: page-with-side-nav
title: Klanten API-standaard
date: 04-05-2022
---
# Klanten API-standaard
API-standaard voor opslaan, bijwerken en toegankelijk maken van gegevens over personen of organisaties waarmee de gemeente contact heeft gehad of (mogelijk) gaat hebben.

# Klantgegevens in relatie tot basisregistraties


# Geïdentificeerde en niet-geïdentificeerde klanten
De Klanten API, bedoeld voor gestandaardiseerd vastleggen van gegevens over klanten, dient twee doelen:
1. Het gestandaardiseerd vastleggen van gegevens die nodig zijn om contact te leggen of onderhouden met Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen, maar niet kunnen worden geregistreerd in de Basisregistratie Personen (BRP) of het Handelsregister (HR). Denk hierbij bijvoorbeeld aan een telefoonnummer of e-mailadres. Deze gegevens worden ook wel ‘aangehaakte’ of ‘plus’gegevens genoemd. Een dergelijke vastlegging leidt tot het ontstaan van een gevalideerde klant.
2. Het vastleggen van gegevens die nodig zijn om contact te leggen of onderhouden met personen in gevallen waar het niet toegestaan, gewenst of nodig is om een contact tussen gemeente en persoon te relateren aan een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR. Denk hierbij aan het ondersteunen van processen waarbinnen geen Burgerservicenummers mogen of hoeven worden verwerkt. Een dergelijke registratie leidt tot het ontstaan van een niet-gevalideerde klant.
a.	Een niet-gevalideerde klant kan na authenticatie een gevalideerde klant worden.

Klanten zijn gerelateerd aan Contactmoment (in de Contactmomenten API) en Verzoek (in de Verzoeken API).

|                                          | geïdentificeerde klant | niet-geïdentificeerde klant |
| ---------------------------------------- | :--------------------: | :-------------------------: |
| relatie met basisregistratiesubject      | :heavy_check_mark:*    | :x:                         |
| geen relatie met basisregistratiesubject | :heavy_check_mark:     | :heavy_check_mark:          |

*na authenticatie met voldoende betrouwbaar middel

De Klanten API bevat resources voor Klant.

# Voorwaarden voor vastlegging
Bij het registreren van gevalideerde klanten horen andere voorwaarden dan bij niet-gevalideerde klanten.
1.	Gevalideerde klant. Het relateren van klantgegevens aan Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen in de BRP of het HR mag alleen plaatsvinden nadat met voldoende zekerheid (middels een authenticatiemiddel van voldoende betrouwbaarheidsniveau) is vastgesteld dat degene die deze gegevens wil (laten) vastleggen het recht heeft dit te (laten) doen.
2.	Niet-gevalideerde klant. Het registreren van klantgegevens zonder relatie naar een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR kan zonder voorwaarden plaatsvinden.

# Betrouwbaarheid en hergebruik
De betrouwbaarheid van vastgelegde klantgegevens wordt bepaald door de mate waarin is na te gaan wíe die gegevens heeft geregistreerd of laten registreren. Deze betrouwbaarheid heeft gevolgen voor de herbruikbaarheid van klantgegevens.
1. Gevalideerde klant. De voorwaarden voor registratie van gevalideerde klanten zorgen ervoor dat we weten wie die gegevens heeft laten vastleggen, en dat deze persoon daartoe gerechtigd was. Daarom kunnen deze gegevens worden beschouwd als betrouwbaar. Bovendien zijn deze klantgegevens op basis van een gegarandeerd unieke sleutel (Burgerservicenummer, RSIN of KvK-nummer) op te vragen. Ze zijn hiermee geschikt voor hergebruik.
2. Niet-gevalideerde klant. Bij niet-gevalideerde klanten is niet na te gaan wie opdracht heeft gegeven tot het vastleggen van klantgegevens. Als (alle) gegevens onjuist blijken te zijn, kan dus niet worden vastgesteld bij wie moet worden aangeklopt om die onjuistheid te herstellen. Hetzelfde geldt als blijkt dat de gegevens van een derde persoon zijn verstrekt – hoewel in dat geval zelfs niet met zekerheid is vast te stellen dat deze derde die gegevens niet toch zelf heeft verstrekt. Niet-gevalideerde klantgegevens moeten daarom worden beschouwd als onbetrouwbaar. Hiermee zijn deze gegevens ook ongeschikt voor hergebruik en alleen te gebruiken wanneer authenticatie

# Klantbeeld
Om redenen van betrouwbaarheid kunnen niet-gevalideerde klantgegevens geen onderdeel uitmaken van een klantbeeld. We weten door het ontbreken van authenticatie voorafgaand aan de oorspronkelijke vastlegging van niet-gevalideerde klantgegevens niet zeker wie die gegevens heeft verstrekt. Gegevens van Gevalideerde klanten kunnen vanzelfsprekend wel onderdeel uitmaken van een klantbeeld.


# Informatie- en gegevensmodel

RGBZ bevat geen resource/objecttype voor Klant. De Klanten API is opgezet in de bredere context van Klantinteractie. Vopor dit domein een apart informatiemodel gemaakt,  geinspireerd op RGBZ. Klant is hierin een nieuw(e) resource/objecttype.

[![Informatiemodel Klanten API](IM Klanten.png){:width="1200px"}](IM Klanten.png "Informatiemodel klanten - klik voor groot")

Het gegevensmodel is een weergave van de implementatie van het informatiemodel in de API specificatie.

[![Gegevensmodel Klanten API](Klanten API 1.0.0b.png){:width="1200px"}](Klanten API 1.0.0b.png "Klanten gegevensmodel - klik voor groot")

### Relatie met contactmomenten

Een klant kan een rol hebben in een contactmoment. Vooralsnog zijn deze rollen `Belanghebbende` en `Gesprekspartner`. De relatie tussen klant en contactmoment is vastgelegd in `klantcontactmoment` in de Contactmomenten API.

### Relatie met verzoeken

Een klant kan een rol hebben bij een verzoek. Vooralsnog zijn deze rollen `Belanghebbende`, `Initiator` en `Mede-initiator`. De relatie tussen klant en contactmoment is vastgelegd in `klantverzoek` in de verzoeken API.

## Specificatie van de Contactmomenten API

* [Referentie-implementatie Klanten API](https://klanten-api.vng.cloud)
* API specificatie (OAS3) in
  [ReDoc](https://klanten-api.vng.cloud/api/v1/schema/),
  [Swagger](https://petstore.swagger.io/?url=https://klanten-api.vng.cloud/api/v1/schema/openapi.yaml),
  [YAML](https://klanten-api.vng.cloud/api/v1/schema/openapi.yaml) of
  [JSON](https://klanten-api.vng.cloud/api/v1/schema/openapi.json)

# Specificatie van gedrag

De Klanten API MOET aan twee aspecten voldoen:

* de OAS-specificatie `openapi.yaml` MOET volledig geïmplementeerd zijn.

* het run-time gedrag hieronder beschreven MOET correct geïmplementeerd zijn.

## OpenAPI specificatie

Alle operaties beschreven in [openapi.yaml](https://klanten-api.vng.cloud/api/v1/schema/openapi.yaml) MOETEN ondersteund worden en tot hetzelfde resultaat leiden als de referentie-implementatie van de KRC.

Het is NIET TOEGESTAAN om gebruik te maken van operaties die niet beschreven staan in deze OAS spec, of om uitbreidingen op operaties in welke vorm dan ook toe te voegen.

## Run-time gedrag

Bepaalde gedrageningen kunnen niet in een OAS spec uitgedrukt worden omdat ze businesslogica bevatten. Deze gedragingen zijn hieronder beschreven en MOETEN zoals beschreven geïmplementeerd worden.

### **<a name="kla-001">Garanderen uniciteit `bronorganisatie` en `klantnummer` van een KLANT ([kla-001](#kla-001))</a>**

Bij het aanmaken (`klant_create`) en bijwerken (`klant_update` en `klant_partial_update`) van een klant MOET gevalideerd worden dat de combinatie `bronorganisatie` en `klantnummer` uniek is, indien het `klantnummer` door de consumer meegestuurd wordt.

Indien het `klantnummer` niet door de consumer gestuurd wordt, dan MOET de Klanten API het nummer genereren op een manier die garandeert dat het uniek is binnen de bronorganisatie.

### **<a name="kla-002">Valideren attribuut `subject` bij aanmaken van een KLANT ([kla-002](#kla-002))</a>**

Bij het aanmaken van een KLANT (`klant_create`) MOET de URL-referentie naar SUBJECT gevalideerd worden op het bestaan indien deze is meegegeven en niet leeg is. Als het ophalen van de objecten niet (uiteindelijk) resulteert in een `HTTP 200` status code, MOET er geantwoord worden met een `HTTP 400` foutbericht.

### HTTP-Caching

De Klanten API moet HTTP-Caching ondersteunen op basis van de `ETag` header. In de API spec staat beschreven voor welke resources dit van toepassing is.

De `ETag` MOET worden berekend op de JSON-weergave van de resource. Verschillende, maar equivalente weergaves (bijvoorbeeld dezelfde API ontsloten wel/niet via NLX) MOETEN verschillende waarden voor de `ETag` hebben.

Indien de consumer een `HEAD` verzoek uitvoert op deze resources, dan MOET de provider antwoorden met dezelfde headers als bij een normale `GET`, dus inclusief de `ETag` header. Er MAG GEEN response body voorkomen.

Indien de consumer gebruik maakt van de `If-None-Match` header, met één of meerdere waarden voor de `ETag`, dan MOET de provider antwoorden met een `HTTP 304` bericht indien de huidige `ETag` waarde van de resource hierin voorkomt. Als de huidige `ETag` waarde hier niet in voorkomt, dan MOET de provider een normale `HTTP 200` response sturen.
