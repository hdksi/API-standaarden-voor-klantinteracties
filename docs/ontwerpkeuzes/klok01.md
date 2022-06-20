---
layout: page-with-side-nav
title: KLOK02: klantgegevens en identificerende gegevens
date: 20-06-2022
---

Onderdeel van klantgevevens zijn zowel de klantgegevens zelf, als een set identificerende gegevens.

1. Klantgegevens: door de klant zelf vestrekte verstrekte gegevens die door de gemeente worden gebruikt om met die klant contact te hebben op een door haar of hem gewenste manier. Het informatiesysteem dat de Klanten API aanbiedt geldt als authentieke bron voor deze gegevens.
2. Identificerende gegevens: één of meerdere gegevens waarmee de gemeente kan vaststellen dat klant gemachtigd is om als of namens een persoon of organisatie te handelen. Het informatiesysteem dat de Klanten API aanbiedt geldt __niet__ als authentieke bron voor deze gegevens. In plaats daarvan gelden identificerende gegevens als een ‘haakje’ naar gegevens die in een andere registratie zijn vastgelegd. Deze andere registratie kan bij de gemeente bekend en direct voor haar toegankelijk zijn, zoals de Basisregistratie Personen of het Nationaal Handelsregister, maar het kan ook gaan om registraties waarvan de gemeente het karakter (nog) niet kent, zoals een buitenlands persoonsregister.

Bij het vastleggen van identificerende gegevens gelden de volgende kardinaliteiten:
1.	Er is (per gemeente) minimaal geen, en maximaal één klant door middel van identificerende gegevens gerelateerd aan een natuurlijk persoon.
2.	Er is (per gemeente) minimaal geen klant gerelateerd aan een niet-natuurlijk persoon, en er is geen maximum in het aantal klanten dat aan een niet-natuurlijk persoon is gerelateerd.
3.	Een klant is gerelateerd aan minimaal geen, en maximaal één natuurlijk persoon óf niet-natuurlijk persoon. Een klant kan dus niet tegelijkertijd aan een natuurlijk persoon én aan een niet-natuurlijk persoon zijn gerelateerd.
