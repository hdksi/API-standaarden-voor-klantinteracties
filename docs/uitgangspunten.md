---
layout: page-with-side-nav
title: Uitgangspunten Klanten API-standaard
date: 09-06-2022
---
# Uitgangspunten bij 'klant'

## Een 'klant' is...

Een klant is een persoon of organisatie waarmee de gemeente contact heeft gehad of (mogelijk) gaat hebben.

## Een 'klant' is _niet_ hetzelfde als een basisregistratiesubject - maar er is wel een relatie

De defintie van klant hierboven kan de vraag oproepen waarom we een klantenregister nodig hebben. Gegevens over personen of organisaties zijn toch al opgeslagen in basisregistraties? Dat klopt. Maar in de Basisregistratie Personen en het Handelsregister vind je van een inwoner of ondernemer geen e-mailadres, telefoonnumer of bankrekeningnummer. Terwijl gemeenten deze gegevens vaak wel nodig hebben, bijvoorbeeld voor het beantwoorden van vragen en het verwerken van aanvragen of meldingen. Gegevens die in een basisregistratie kunnen opgenomen, maar wel ‘horen’ bij een in een basisregistratie geregistreerd subject of object noemen we wel  ‘aangehaakte’ of ‘plus’gegevens.

Gegevens die gemeenten in staat stellen met inwoners of ondernemers zijn een voorbeeld van ‘aangehaakte’ of ‘plus’gegevens. Ze zijn immers direct te relateren aan een (natuurlijk of niet-natuurlijk) persoon. De relatie tussen zo'n persoon in een basisregistratie en een ‘klant’ kan in het klantenregister dan ook concreet worden vastgelegd. Dit gebeurt door middel van een (url-)verwijzing naar een speciefiek subject in een basisregistratie, of - als verwijzen niet mogelijk is - door het overnemen uit die basisregistratie van een beperkt aantal identificerende gegevens. Na het leggen van zo'n relatie is een ‘aangehaakte’ klant ontstaan. Voor de relatie tussen subjecten in basisregistraties en klanten gelden de volgende kardinaliteiten:

1.	Er is (per gemeente) minimaal geen (nul) en maximaal één aangehaakte klant gekoppeld aan één Natuurlijk Persoon in de Basisregistratie Personen.
2.	Er zijn (per organisatie) minimaal geen (nul) aangehaakte klanten gekoppeld aan één Niet-Natuurlijk Persoon of Vestiging in het Handelsregister en er is geen beperking aan het maximale aantal aangehaakte klanten dat aan één Niet-Natuurlijk Persoon of Vestiging is gerelateerd.
3.	Een aangehaakte klant kan aan maximaal één Natuurlijk Persoon in de  Basisregistratie Personen of aan één Niet-Natuurlijk Persoon of Vestiging in het Handelsregister zijn gekoppeld. Een klant kan dus niet tegelijkertijd aan een Natuurlijk Persoon in de Basisregistratie Personen én aan een Niet-Natuurlijk Persoon of Vestiging in het Handelsregister zijn gerelateerd.

Bovenstaande betekent dat klantgegevens geen reparatiemiddel zijn voor onjuiste gegevens in basisregistraties. Als geconstateerd wordt dat gegevens in de basisregistraties onjuist zijn, moet deze onjuistheid aan de beheerder van die basisregistratie worden (terug)gemeld.

## Klantgegevens hoeven niet overeen te komen met gegevens in basisregistraties

Klantgegevens hoeven niet overeen te stemmen met ‘equivalente’ gegevens in basisregistraties. Een klant die in het dagelijks leven bijvoorbeeld een voornaam gebruikt die afwijkt van de voornaam die in de Basisregistratie Personen is vastgelegd, kan bij het opgeven van klantgegevens zelf bepalen met welke voornaam zij of hij wil worden aangesproken. Ook een opgegeven adres hoeft niet overeen te komen met (een van de) in de basisregistratie opgenomen adressen. Een door de klant opgegeven adres is immers te zien als diens ‘voorkeurscorrespondentie- of bezoekadres’.

Registratie van klantgegevens betekent niet dat een inwoner of ondernemer het recht verwerft altijd op basis van de klantgegevens met de gemeente te communiceren. Als de aard van de interactie bijvoorbeeld vereist dat correspondentie naar het in de Basisregistratie Personen bekende verblijfsadres gestuurd wordt, kan en mag die correspondentie immers niet aan een daarvan afwijkend ‘voorkeursadres’ worden geadresseerd.

# We onderscheiden aangehaakte en zelfstandige klanten

Uit de bovenstaande uitgangspunten volgt dat er ‘aangehaakte’ klanten bestaan. Maar klantgegevens kunnen ook worden vastgelegd zonder dat sprake is van een relatie tussen een klant en subjectgegevens in een basisregistratie. Dit betekent dat twee ‘typen’ klant onderscheiden kunnen worden, namelijk:

1. __Aangehaakte klant.__ Een klant waarvan klantgegevens zijn gerelateerd aan een basisregistratiesubject. Klantgegevens dienen hier om contact te leggen of onderhouden met Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen op basis van gegevens die niet kunnen worden geregistreerd in de Basisregistratie Personen of het Handelsregister.
2. __Zelfstandige klant.__ Een klant waarvan klantgegevens niet zijn gerelateerd aan een basisregistratiesubject. In dit geval dienen klantgegevens om contact te leggen of onderhouden met inwoners of ondernemers in gevallen waar het niet toegestaan, gewenst of nodig is om een contact tussen gemeente en persoon te relateren aan een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR. Denk hierbij aan het ondersteunen van processen waarbinnen geen Burgerservicenummers mogen of hoeven worden verwerkt.

Voor verschillende 'typen' klant gelden verschillende hieronder beschreven uitgangspunten.

## Zelfstandige klanten kunnen zonder voorwaarden worden geregistreerd, aangehaakte klanten niet

Voor het registreren en verstrekken van gegevens over aangehaakte klanten gelden andere voorwaarden dan bij zelfstandige klanten:

1.	__Aangehaakte klant.__ Het relateren van klantgegevens aan Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen in de Basisregistratie Personen, het Handelsregister of eventueel een buitenlandse (basis)registratie mag alleen nadat met voldoende zekerheid (dus middels een authenticatiemiddel van voldoende betrouwbaarheidsniveau) is vastgesteld dat degene die deze gegevens wil (laten) vastleggen gemachtigd is dit te (laten) doen. Voordat eerder geregistreerde gegevens aan de klant verstrekt worden, moet opnieuw met voldoende zekerheid zijn vastgesteld of degene aan wie deze verstrekt worden daartoe gemachtigd is.
2.	__Zelfstandige klant.__ Registratie van klantgegevens zonder relatie naar een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR kan zonder voorwaarden plaatsvinden. Opnieuw verstrekken kan alleen binnen de context van de interactie waarvoor de gegeven verstrekt zijn (zie ook uitgangspunt over _hergebruik_ hieronder).

Voor registreren van klantgegevens geldt dus:

|                               | Na identificatie/authenticatie             | Zonder identificatie/authenticatie        |
| ----------------------------- | ------------------------------------------ | ----------------------------------------- |
| Aangehaakte klant             | :heavy_check_mark: registratie toegestaan* | :x: registratie niet toegestaan           |
| Zelfstandige klant            | :heavy_check_mark: registratie toegestaan  | :heavy_check_mark: registratie toegestaan |

*na toepassing van voldoende betrouwbaar middel.

En voor verstrekken geldt:

|                               | Na identificatie/authenticatie                                                                                           | Zonder identificatie/authenticatie                                                                                                                      |
| ----------------------------- | ------------------------------------------                                                                               | -----------------------------------------                                                                                                                             |
| Aangehaakte klant             | :heavy_check_mark: verstrekken toegestaan*                                                                               | :x: verstrekken niet toegestaan                                                                                                                         |
| Zelfstandige klant            | :heavy_exclamation_mark: verstrekken alleen toegestaan in de context van de interactie waarvoor gegevens zijn ingewonnen | :heavy_check_mark: registratie toegestaan:heavy_exclamation_mark: verstrekken alleen toegestaan in de context van de interactie waarvoor gegevens zijn ingewonnen |

## Gegevens over zelfstandige klanten zijn onbetrouwbaar en ongeschikt voor hergebruik

De betrouwbaarheid van vastgelegde klantgegevens wordt bepaald door de mate waarin is na te gaan wíe die gegevens heeft geregistreerd of laten registreren. Deze betrouwbaarheid heeft gevolgen voor de herbruikbaarheid van klantgegevens.

1. __Aangehaakte klant.__ Door de voorwaarden voor registratie weten we wie die de klantgegevens heeft laten vastleggen, en kunnen we vaststellen dat deze persoon daartoe gerechtigd was. Daarom kunnen deze gegevens worden beschouwd als betrouwbaar. Bovendien zijn deze klantgegevens meestal op basis van een gegarandeerd unieke sleutel (Burgerservicenummer, RSIN of KvK-nummer) op te vragen. Ze zijn hiermee geschikt voor hergebruik. _De voorwaarden waaronder dit hergebruik is toegestaan is ondewerp van onderzoek._
2. __Zelfstandige klant.__ Hier is niet na te gaan wie opdracht heeft gegeven tot het vastleggen van klantgegevens. Als (alle) gegevens onjuist blijken te zijn, kan dus niet worden vastgesteld bij wie moet worden aangeklopt om die onjuistheid te herstellen. Hetzelfde geldt als blijkt dat de gegevens van een derde persoon zijn verstrekt – hoewel in dat geval zelfs niet met zekerheid is vast te stellen dat deze derde die gegevens niet toch zelf heeft verstrekt. Zelfstandige klantgegevens moeten daarom - ongeacht de intentie van verstrekker - worden beschouwd als onbetrouwbaar. Hiermee zijn deze gegevens ook ongeschikt voor gebruik buiten de context van de interactie waarvoor ze zijn ingewonnen. Dit betekent dus ook dat klantgegevens bij een volgende interactie opnieuw moeten worden ingewonnen!

## Gegevens over zelfstandige klanten zijn geen onderdeel van het klantbeeld

Omdat gegevens over zelfstandige klanten ongeschikt zijn voor hergebruik buiten de context van de interactie waarvoor ze zijn ingewonnen, kunnen ze geen onderdeel zijn van een klantbeeld. Dat zou immers voor iedere zelfstandige klant beperkt zijn tot één interactie. Gegevens van Gevalideerde klanten kunnen vanzelfsprekend wel onderdeel uitmaken van een klantbeeld.

## We leggen niet meer (klant)gegevens vast dan nodig

Klantgegevens worden alleen vastgelegd als dat vanwege het karakter van de interactie nodig is, of als de klant aangeeft dat te willen. Dit betekent dat een eenvoudige melding vaak zonder registratie van enig klantgegeven kan worden opgeslot, terwijl als de klant over de oplossing van die melding op de hoogte gehouden wil worden volstaan kan worden met registratie van een (voor)naam en telefoonnummer of e-mailadres. Dit uitgangspunt geldt ook voor het relateren van een klant aan een subject in een basisregistratie - waarmee dus een aangehaakte klant ontstaat. Als zo'n relatie niet nodig of door de klant zelf gewenst is, wordt die niet gelegd.

## Klantgegevens zijn 'van de klant'

Hoewel gegevens juridisch geen eigenaar (kunnen) kennen, is het uitgangspunt dat klantgegevens ‘van de klant zijn’. Dit betekent dat een inwoner of ondernemer zoveel mogelijk zelf haar of zijn klantgegevens verstrekt, en in staat wordt gesteld eerder verstrekte gegevens aan te passen of - voor zover de bewaartermijn van eventueel aan de klant gerelateerde zaak(dossiers) dat toelaat - te verwijderen. Op termijn zouden klantgegevens in het kader van ['regie op gegevens'](https://www.digitaleoverheid.nl/overzicht-van-alle-onderwerpen/regie-op-gegevens/) zelfs geheel uit de gemeentelijke administratie kunnen verdwijnen om in plaats daarvan door de klant zelf te worden bewaard en beheerd.

## Klantgegevens worden op het juiste moment vernietigd

Aangehaakte en zelfstandige klanten kennen een verschillend vernietigingsregime:

1. __Aangehaakte klant.__ _De bewaartermijn voor aangehaakte klanten is onderwerp van onderzoek._
2. __Zelfstandige klant.__ Gegevens over zelfstandige klanten zijn onderdeel van het (zaak)dossier dat aanleiding gaf voor de registratie van die klantgegevens en worden dus vernietigd op het moment dat de bewaartermijn van dat dossier is verlopen.
