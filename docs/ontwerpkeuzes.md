---
layout: page-with-side-nav
title: Ontwerpkeuzes API-standaarden voor Klantinteracties
date: 20-06-2022
---

# Klanten

## KLOK01 - Klantgegevens kunnen identificerende gegevens omvatten

### Relevante Uitgangspunten

### Keuze

Klantgevevens kunnen naast de klantgegevens zelf, ook een set identificerende gegevens omvatten.

### Rationale
Klantgegevens zijn persoonsgegevens. Om inzage te kunnen gegeven in eerder vastgelegde klantgegevens is het daarom nodig dat de gemeente kan vaststellen dat zij contact heeft met de persoon of organisatie die de eerder vastgelede klantgegevens heeft verstrekt, óf met een persoon of organisatie die gemachtigd is de in te zien of te wijzigen. Het vastleggen van identificerende gegevens dient dit doel.

### Toelichting
In de Klanten API kunnen zowel klantgegevens als identificerende gegevens worden vastgelegd:

1. Klantgegevens: door de klant zelf vestrekte verstrekte gegevens die door de gemeente worden gebruikt om met die klant contact te hebben op een door haar of hem gewenste manier. Het informatiesysteem dat de Klanten API aanbiedt geldt als authentieke bron voor deze gegevens.
2. Identificerende gegevens: één of meerdere gegevens waarmee de gemeente kan vaststellen dat klant gemachtigd is om als of namens een persoon of organisatie te handelen. Het informatiesysteem dat de Klanten API aanbiedt geldt __niet__ als authentieke bron voor deze gegevens. In plaats daarvan gelden identificerende gegevens als een ‘haakje’ naar gegevens die in een andere registratie zijn vastgelegd. Deze andere registratie kan bij de gemeente bekend en direct voor haar toegankelijk zijn, zoals in het geval van de Basisregistratie Personen of het Nationaal Handelsregister, maar het kan ook gaan om een registratie waarvan de gemeente het karakter (nog) niet kent, zoals een buitenlands persoonsregister.

Als als onderdeel van de klantgegevens (voldoende) identificerende gegevens zijn vastgelegd, spreken we van een [Aangehaakte klant](/begrippen.md#aangehaakte-klant). In andere gevallen is sprake van een [Zelfstandige klant](/begrippen.md#zelfstandige-klant).

Bij de relaties tussen klanten en (identificerende gegevens over) natuurlijke of niet-natuurlijke personen gelden de volgende kardinaliteiten:

1.	Er is (per gemeente) minimaal geen, en maximaal één klant door middel van identificerende gegevens gerelateerd aan een natuurlijk persoon.
2.	Er is (per gemeente) minimaal geen klant gerelateerd aan een niet-natuurlijk persoon, en er is geen maximum in het aantal klanten dat aan een niet-natuurlijk persoon is gerelateerd.
3.	Een klant is gerelateerd aan minimaal geen, en maximaal één natuurlijk persoon óf niet-natuurlijk persoon. Een klant kan dus niet tegelijkertijd aan een natuurlijk persoon én aan een niet-natuurlijk persoon zijn gerelateerd.

### Implicaties

#### Voor het vastleggen van identificerende gegevens zi

1.	__Aangehaakte klant.__ Het vastleggen van identificerende gegevens mag alleen nadat met voldoende zekerheid (dus middels een authenticatiemiddel van voldoende betrouwbaarheidsniveau) is vastgesteld dat degene die deze gegevens wil (laten) vastleggen gemachtigd is dit te (laten) doen. Voordat eerder geregistreerde gegevens aan de klant verstrekt worden, moet opnieuw met voldoende zekerheid zijn vastgesteld of degene aan wie deze verstrekt worden daartoe gemachtigd is.
2.	__Zelfstandige klant.__ Registratie van klantgegevens zonder relatie naar een Natuurlijk of (vertegenwoordiger van) Niet-natuurlijk persoon in de BRP of het HR kan zonder voorwaarden plaatsvinden. Opnieuw verstrekken kan alleen binnen de context van de interactie waarvoor de gegeven verstrekt zijn (zie ook uitgangspunt over _hergebruik_ hieronder).

Voor registreren en verestrekken van klantgegevens geldt dus:

|                               | Na identificatie/authenticatie | Zonder identificatie/authenticatie |
| ----------------------------- | ------------------------------ | ---------------------------------- |
| Aangehaakte klant             | :heavy_check_mark: registratie toegestaan¹<br>:heavy_check_mark: verstrekken toegestaan¹  | :x: registratie niet toegestaan<br>:x: verstrekken niet toegestaan |
| Zelfstandige klant            | :heavy_check_mark: registratie toegestaan<br>:grey_exclamation: verstrekken alleen toegestaan binnen de interactie waarvoor ingewonnen | :heavy_check_mark: registratie toegestaan<br>:grey_exclamation: verstrekken alleen toegestaan binnen de interactie waarvoor ingewonnen  |

¹na toepassing van voldoende betrouwbaar middel.

#### Gegevens over zelfstandige klanten zijn onbetrouwbaar en ongeschikt voor hergebruik

De betrouwbaarheid van vastgelegde klantgegevens wordt bepaald door de mate waarin is na te gaan wíe die gegevens heeft geregistreerd of laten registreren. Deze betrouwbaarheid heeft gevolgen voor de herbruikbaarheid van klantgegevens.

1. __Aangehaakte klant.__ Door de voorwaarden voor registratie weten we wie die de klantgegevens heeft laten vastleggen, en kunnen we vaststellen dat deze persoon daartoe gerechtigd was. Daarom kunnen deze gegevens worden beschouwd als betrouwbaar. Bovendien zijn deze klantgegevens meestal op basis van een gegarandeerd unieke sleutel (Burgerservicenummer, RSIN of KvK-nummer) op te vragen. Ze zijn hiermee geschikt voor hergebruik. _De voorwaarden waaronder dit hergebruik is toegestaan is ondewerp van onderzoek._
2. __Zelfstandige klant.__ Hier is niet na te gaan wie opdracht heeft gegeven tot het vastleggen van klantgegevens. Als (alle) gegevens onjuist blijken te zijn, kan dus niet worden vastgesteld bij wie moet worden aangeklopt om die onjuistheid te herstellen. Hetzelfde geldt als blijkt dat de gegevens van een derde persoon zijn verstrekt – hoewel in dat geval zelfs niet met zekerheid is vast te stellen dat deze derde die gegevens niet toch zelf heeft verstrekt. Zelfstandige klantgegevens moeten daarom - ongeacht de intentie van verstrekker - worden beschouwd als onbetrouwbaar. Hiermee zijn deze gegevens ook ongeschikt voor gebruik buiten de context van de interactie waarvoor ze zijn ingewonnen. Dit betekent dus ook dat klantgegevens bij een volgende interactie opnieuw moeten worden ingewonnen en dat het niet mogelijk is van een zelfstandige klant na registratie een aangehaakte klant te maken.

#### Gegevens over zelfstandige klanten zijn geen onderdeel van het klantbeeld

Omdat gegevens over zelfstandige klanten ongeschikt zijn voor hergebruik buiten de context van de interactie waarvoor ze zijn ingewonnen, kunnen ze geen onderdeel zijn van een klantbeeld. Dat zou immers voor iedere zelfstandige klant beperkt zijn tot één interactie. Gegevens van Gevalideerde klanten kunnen vanzelfsprekend wel onderdeel uitmaken van een klantbeeld.
