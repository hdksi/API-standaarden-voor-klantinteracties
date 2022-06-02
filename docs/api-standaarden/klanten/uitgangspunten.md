---
layout: page-with-side-nav
title: Uitgangspunten Klanten API-standaard
date: 02-06-2022
---
# Klanten API-standaard
Voor het leveren van producten en diensten aan inwoners en ondenemers hebben gemeenten (contact)gegevens van die inwoners en ondernemers nodig. Denk hierbij aan adresgegevens, een telefoonnumer of e-mailadres, een bankrekeningnummer, maar ook aan voorkeuren ten aanzien van het kanaal dat dat de gemeenten gebruikt om contact op te nemen. Een deel van deze gegevens is beschikbaar in de Basisregistratie Personen (BRP) en het Nationaal Handelsregister (HR). Daarbij geldt echter dat:
1. De gegevens die in de basisregistratie zijn vastgelegd niet altijd overeenkomen met de, en
2. Niet iedereen waarmee de gemeente zaken doet bekend is in zo'n basisregistratie.

## Eigenaarschap
Hoewel gegevens juridisch geen eigenaar (kunnen) kennen, is het uitgangspunt dat klantgegevens 'van de klant zijn'. Dit betekent dat een inwoner of ondernemer waar mogelijk zelf zijn klantgegevens verstrekt, en dat die gegevens door kan aanpassen of verwijderen. Dit betekent ook dat deze gegevens later een goede kandidaat zijn voor Regie op Gegevensdiensten en uiteindelijk opslag bij de inwoner of ondernemer zelf.

## Klanten API-standaard
API-standaard voor opslaan, bijwerken en toegankelijk maken van gegevens over personen of organisaties waarmee de gemeente contact heeft gehad of (mogelijk) gaat hebben.

## Klantgegevens in relatie tot subjectgegevens in basisregistraties
Klantgegevens worden geregistreerd met als doel het vergemakkelijken van communicatie met de gemeente. Dit doel verschilt fundamenteel van de doelen waarmee gegevens in de BRP en het HR worden vastgelegd. Dit komt tot uitdrukking in een tweetal uitgangspunten bij de relatie tussen gegevens in basisregistraties en gerelateerde klantgegevens.
Uitgangspunten
1. Klantgegevens zijn geen reparatiemiddel voor onjuiste gegevens in basisregistraties. Als geconstateerd wordt dat gegevens in de basisregistraties onjuist zijn, moet deze onjuistheid aan de beheerder van die basisregistratie worden (terug)gemeld.
2.	Klantgegevens hoeven niet overeen te stemmen met ‘equivalente’ gegevens in basisregistraties. Bijvoorbeeld: een persoon hanteert in het dagelijks leven een voornaam die afwijkt van de voornaam die in de BRP is vastgelegd. Bij de registratie van klantgegevens kan de persoon zelf kiezen welke voornaam wordt vastgelegd. Ook het opgegeven adres hoeft niet overeen te komen met in de BRP of het HR geregistreerde adressen.  Het adres van de klant is immers te zien als diens ‘voorkeurscorrespondentieadres’. Als processen vereisen dat correspondentie bijvoorbeeld naar het in de BRP bekende verblijfsadres van een Natuurlijk Persoon wordt gestuurd, wordt daarmee het gebruik van dit ‘voorkeurscorrespondentieadres’ uiteraard overruled.

###Relatie naar basisregistraties: kardinaliteit
1.	Er is (per organisatie) minimaal geen (nul) en maximaal één gevalideerde klant gekoppeld aan één Natuurlijk Persoon in de Basisregistratie Personen.
2.	Er zijn (per organisatie) minimaal geen (nul) klanten gekoppeld aan één Niet-Natuurlijk Persoon of Vestiging in het Handelsregister. Er is geen beperking aan het maximale aantal klanten dat aan één Niet-Natuurlijk Persoon of Vestiging is gerelateerd.
3.	Een klant kan aan maximaal één Natuurlijk Persoon in de BRP of aan één Niet-Natuurlijk Persoon of Vestiging in het Handelsregister zijn gekoppeld. Een klant kan dus niet tegelijkertijd aan een Natuurlijk Persoon in de BRP én aan een Niet-Natuurlijk Persoon of Vestiging in het Handelsregister zijn gerelateerd.

# Geïdentificeerde en niet-geïdentificeerde klanten
De Klanten API, bedoeld voor gestandaardiseerd vastleggen van gegevens over klanten, dient twee doelen:
1. Het gestandaardiseerd vastleggen van gegevens die nodig zijn om contact te leggen of onderhouden met Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen, maar niet kunnen worden geregistreerd in de Basisregistratie Personen (BRP) of het Handelsregister (HR). Denk hierbij bijvoorbeeld aan een telefoonnummer of e-mailadres. Deze gegevens worden ook wel ‘aangehaakte’ of ‘plus’gegevens genoemd. Een dergelijke vastlegging leidt tot het ontstaan van een gevalideerde klant.
2. Het vastleggen van gegevens die nodig zijn om contact te leggen of onderhouden met personen in gevallen waar het niet toegestaan, gewenst of nodig is om een contact tussen gemeente en persoon te relateren aan een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR. Denk hierbij aan het ondersteunen van processen waarbinnen geen Burgerservicenummers mogen of hoeven worden verwerkt. Een dergelijke registratie leidt tot het ontstaan van een niet-gevalideerde klant.
a.	Een niet-gevalideerde klant kan na authenticatie een gevalideerde klant worden.

Klanten zijn gerelateerd aan Contactmoment (in de Contactmomenten API) en Verzoek (in de Verzoeken API).

|                                                    | geïdentificeerde klant         | niet-geïdentificeerde klant   |
| -------------------------------------------------- | ------------------------------ | ----------------------------- |
| klant gerelateerd aan basisregistratiesubject      | :heavy_check_mark: toegestaan* | :heavy_check_mark: toegestaan |
| klant niet gerelateerd aan basisregistratiesubject | :x: niet toegestaan            | :heavy_check_mark: toegestaan |

*na authenticatie met voldoende betrouwbaar middel

De Klanten API bevat resources voor Klant.

## Voorwaarden voor vastlegging
Bij het registreren van gevalideerde klanten horen andere voorwaarden dan bij niet-gevalideerde klanten.
1.	Gevalideerde klant. Het relateren van klantgegevens aan Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen in de BRP of het HR mag alleen plaatsvinden nadat met voldoende zekerheid (middels een authenticatiemiddel van voldoende betrouwbaarheidsniveau) is vastgesteld dat degene die deze gegevens wil (laten) vastleggen het recht heeft dit te (laten) doen.
2.	Niet-gevalideerde klant. Het registreren van klantgegevens zonder relatie naar een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR kan zonder voorwaarden plaatsvinden.

## Betrouwbaarheid en hergebruik
De betrouwbaarheid van vastgelegde klantgegevens wordt bepaald door de mate waarin is na te gaan wíe die gegevens heeft geregistreerd of laten registreren. Deze betrouwbaarheid heeft gevolgen voor de herbruikbaarheid van klantgegevens.
1. Gevalideerde klant. De voorwaarden voor registratie van gevalideerde klanten zorgen ervoor dat we weten wie die gegevens heeft laten vastleggen, en dat deze persoon daartoe gerechtigd was. Daarom kunnen deze gegevens worden beschouwd als betrouwbaar. Bovendien zijn deze klantgegevens op basis van een gegarandeerd unieke sleutel (Burgerservicenummer, RSIN of KvK-nummer) op te vragen. Ze zijn hiermee geschikt voor hergebruik.
2. Niet-gevalideerde klant. Bij niet-gevalideerde klanten is niet na te gaan wie opdracht heeft gegeven tot het vastleggen van klantgegevens. Als (alle) gegevens onjuist blijken te zijn, kan dus niet worden vastgesteld bij wie moet worden aangeklopt om die onjuistheid te herstellen. Hetzelfde geldt als blijkt dat de gegevens van een derde persoon zijn verstrekt – hoewel in dat geval zelfs niet met zekerheid is vast te stellen dat deze derde die gegevens niet toch zelf heeft verstrekt. Niet-gevalideerde klantgegevens moeten daarom worden beschouwd als onbetrouwbaar. Hiermee zijn deze gegevens ook ongeschikt voor hergebruik en alleen te gebruiken wanneer authenticatie

## Klantbeeld
Om redenen van betrouwbaarheid kunnen niet-gevalideerde klantgegevens geen onderdeel uitmaken van een klantbeeld. We weten door het ontbreken van authenticatie voorafgaand aan de oorspronkelijke vastlegging van niet-gevalideerde klantgegevens niet zeker wie die gegevens heeft verstrekt. Gegevens van Gevalideerde klanten kunnen vanzelfsprekend wel onderdeel uitmaken van een klantbeeld.
