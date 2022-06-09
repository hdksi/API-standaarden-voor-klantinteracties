---
layout: page-with-side-nav
title: Uitgangspunten Klanten API-standaard
date: 09-06-2022
---
# Uitgangspunten bij 'klant'

## Een 'klant' is...

Een klant is een persoon of organisatie waarmee de gemeente contact heeft gehad of (mogelijk) gaat hebben.

## Een 'klant' is _niet_ hetzelfde als een basisregistratiesubject - maar er is wel een relatie

Gegevens over personen of organisaties zijn toch ogeslagen in basisregistraties? Dat klopt. Maar het doel van bijhouden van gegevens in de Basisregistratie Personen (BRP) en het Handelsregister (HR) verschilt sterk van het doel van vergemakkelijken van communicatie met de gemeente waarmee klantgegevens worden geregistreerd. Dit afwijkende doel heeft zijn weerslag op gegevens die in de basisregistraties geregistreerd (kunnen) worden. Daarin vind je van een inwoner geen e-mailadres, telefoonnumer of bankrekeningnummer - gegevens die ook wel  ‘aangehaakte’ of ‘plus’gegevens worden genoemd. Klantgegevens 'haken' dan ook - als dat nodig is - aan bij gegevens over over het bijbehorende subject in een basisregistratie. Om deze relatie te leggen kan in het klantenregister een (url-)verwijzing naar een subject in een basisregistratie worden vastgelegd, of kunnen daarin - als verwijzen niet mogelijk is - een beperkt aantal identificerende (basis)gegevens worden overgenomen. Voor deze relaties gelden de volgende kardinaliteiten:

1.	Er is (per gemeente) minimaal geen (nul) en maximaal één gevalideerde klant gekoppeld aan één Natuurlijk Persoon in de Basisregistratie Personen.
2.	Er zijn (per organisatie) minimaal geen (nul) klanten gekoppeld aan één Niet-Natuurlijk Persoon of Vestiging in het Handelsregister en er is geen beperking aan het maximale aantal klanten dat aan één Niet-Natuurlijk Persoon of Vestiging is gerelateerd.
3.	Een klant kan aan maximaal één Natuurlijk Persoon in de  Basisregistratie Personen of aan één Niet-Natuurlijk Persoon of Vestiging in het Handelsregister zijn gekoppeld. Een klant kan dus niet tegelijkertijd aan een Natuurlijk Persoon in de BRP én aan een Niet-Natuurlijk Persoon of Vestiging in het Handelsregister zijn gerelateerd.

Bovenstaande betekent dat klantgegevens geen reparatiemiddel zijn voor onjuiste gegevens in basisregistraties. Als geconstateerd wordt dat gegevens in de basisregistraties onjuist zijn, moet deze onjuistheid aan de beheerder van die basisregistratie worden (terug)gemeld.

## Klantgegevens hoeven niet overeen te komen met gegevens in basisregistraties

Klantgegevens hoeven niet overeen te stemmen met ‘equivalente’ gegevens in basisregistraties. Een klant die in het dagelijks leven bijvoorbeeld een voornaam gebruikt die afwijkt van de voornaam die in de BRP is vastgelegd kan bij de registratie van klantgegevens bepalen welke voornaam wordt vastgelegd. Ook een opgegeven adres hoeft niet overeen te komen met in de BRP of het HR geregistreerde adressen. Een door de klant opgegeven adres is immers te zien als diens ‘voorkeurscorrespondentie- of bezoekadres’. Maar als de aard van de interactie vereist dat correspondentie bijvoorbeeld naar het in de BRP bekende verblijfsadres van een Natuurlijk Persoon wordt gestuurd, mag die correspondentie uiteraard niet aan zo'n - daarvan afwijkend - ‘voorkeursadres’ worden geadresseerd.

## We leggen niet meer (klant)gegevens vast dan nodig

Klantgegevens worden alleen vastgelegd als dat vanwege het karakter van de interactie nodig is, of als de klant aangeeft dat te willen. Dit betekent dat een eenvoudige melding vaak zonder registratie van enig klantgegeven kan worden opgeslot, terwijl als de klant over de oplossing van die melding op de hoogte gehouden wil worden volstaan kan worden met registratie van een (voor)naam en telefoonnummer of e-mailadres. Dit uitgangspunt geldt ook voor het relateren van een klant aan een subject in een basisregistratie. Als zo'n relatie niet nodig of door de klant zelf gewenst is, wordt die niet gelegd.

## Klantgegevens zijn 'van de klant'

Hoewel gegevens juridisch geen eigenaar (kunnen) kennen, is het uitgangspunt dat klantgegevens 'van de klant zijn'. Dit betekent dat een inwoner of ondernemer waar mogelijk zelf zijn klantgegevens verstrekt, en ook zelf eerder verstrekte gegevens kan aanpassen of verwijderen. Op termijn zouden klantgegevens in het kader van ['regie op gegevens'](https://www.digitaleoverheid.nl/overzicht-van-alle-onderwerpen/regie-op-gegevens/) zelfs geheel uit de gemeentelijke administratie kunnen verdwijnen om in plaats daarvan door de klant zelf te worden bewaard en beheerd.

# We onderscheiden aangehaakte en zelfstandige klanten

Uit de bovenstaande uitgangspunten volgt dat er twee 'type' klanten bestaan.
1. __Aangehaakte klant.__ Een klant waarvan klantgegevens zijn gerelateerd aan een basisregistratiesubject. Klantgegevens dienen hier om contact te leggen of onderhouden met Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen op basis van gegevens die niet kunnen worden geregistreerd in de Basisregistratie Personen (BRP) of het Handelsregister (HR).
2. __Zelfstandige klant.__ Een klant waarvan klantgegevens niet zijn gerelateerd aan een basisregistratiesubject. In dit geval dienen klantgegevens om contact te leggen of onderhouden met inwoners of ondernemers in gevallen waar het niet toegestaan, gewenst of nodig is om een contact tussen gemeente en persoon te relateren aan een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR. Denk hierbij aan het ondersteunen van processen waarbinnen geen Burgerservicenummers mogen of hoeven worden verwerkt.

Voor verschillende 'typen' klant gelden verschillende hieronder beschreven uitgangspunten.

## Voor registratie van aangehaakte en zelfstandige klanten gelden verschillende voorwaarden

Voor het registreren en verstrekt van gegevens over geïdentificeerde klanten gelden andere voorwaarden dan voor niet-geïdentificeerde klanten:
1.	__Aangehaakte klant.__ Het relateren van klantgegevens aan Natuurlijke of (vertegenwoordigers van) Niet-natuurlijke personen in de BRP of het HR mag alleen plaatsvinden nadat met voldoende zekerheid (middels een authenticatiemiddel van voldoende betrouwbaarheidsniveau) is vastgesteld dat degene die deze gegevens wil (laten) vastleggen het recht heeft dit te (laten) doen. Voordat eerder geregistreerde gegevens aan de klant verstrekt worden, moet met voldoende zekerheid zijn vastgesteld of degene aan wie deze verstrekt worden gerechtigid is deze in te zien.
2.	__Zelfstandige klant.__ Registratie van klantgegevens zonder relatie naar een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR kan zonder voorwaarden plaatsvinden. Opnieuw verstrekken kan alleen binnen de context van de interactie waarvoor de gegeven verstrekt zijn (zie ook uitgangspunt over _hergebruik_ hieronder).

Onderstaande de voorwaarden voor registratie van Aangehaakte en zelfstandige klanten na en zonder identificatie/authenticatie:
|                               | Na identificatie/authenticatie             | Zonder identificatie/authenticatie        |
| ----------------------------- | ------------------------------------------ | ----------------------------------------- |
| Aangehaakte klant             | :heavy_check_mark: registratie toegestaan* | :x: registratie niet toegestaan           |
| Zelfstandige klant            | :heavy_check_mark: registratie toegestaan  | :heavy_check_mark: registratie toegestaan |

*mits voldoende betrouwbaar middel toegepast

## We beschouwen gegevens over zelfstandige klanten als onbetrouwbaar en ongeschikt voor hergebruik

De betrouwbaarheid van vastgelegde klantgegevens wordt bepaald door de mate waarin is na te gaan wíe die gegevens heeft geregistreerd of laten registreren. Deze betrouwbaarheid heeft gevolgen voor de herbruikbaarheid van klantgegevens.
1. __Aangehaakte klant.__ Door de voorwaarden voor registratie weten we wie die de klantgegevens heeft laten vastleggen, en kunnen we vaststellen dat deze persoon daartoe gerechtigd was. Daarom kunnen deze gegevens worden beschouwd als betrouwbaar. Bovendien zijn deze klantgegevens op basis van een gegarandeerd unieke sleutel (Burgerservicenummer, RSIN of KvK-nummer) op te vragen. Ze zijn hiermee geschikt voor hergebruik.
2. __Zelfstandige klant.__ Hier is niet na te gaan wie opdracht heeft gegeven tot het vastleggen van klantgegevens. Als (alle) gegevens onjuist blijken te zijn, kan dus niet worden vastgesteld bij wie moet worden aangeklopt om die onjuistheid te herstellen. Hetzelfde geldt als blijkt dat de gegevens van een derde persoon zijn verstrekt – hoewel in dat geval zelfs niet met zekerheid is vast te stellen dat deze derde die gegevens niet toch zelf heeft verstrekt. Zelfstandige klantgegevens moeten daarom - ongeacht de intentie van verstrekker - worden beschouwd als onbetrouwbaar. Hiermee zijn deze gegevens ook ongeschikt voor hergebruik.

## Gegevens over zelfstandige klanten zijn geen onderdeel van het klantbeeld

Om redenen van betrouwbaarheid kunnen niet-geïdentificeerde klantgegevens geen onderdeel uitmaken van een klantbeeld. We weten door het ontbreken van authenticatie voorafgaand aan de oorspronkelijke vastlegging van niet-gevalideerde klantgegevens niet zeker wie die gegevens heeft verstrekt. Gegevens van Gevalideerde klanten kunnen vanzelfsprekend wel onderdeel uitmaken van een klantbeeld.
