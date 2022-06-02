---
layout: page-with-side-nav
title: Productvisie API-standaarden voor Klantinteracties
date: 02-06-2022
---
# Introductie
In 2019 zijn de [API-standaarden voor Zaakgericht werken](https://vng-realisatie.github.io/gemma-zaken/) vastgesteld. Als 'spin-off' van dat ontwikkeltraject zijn ook de eerste stappen gezet van de ontwikkeling van drie daaraan gerelateerde API-standaarden voor Klanten, Contactmomenten en Productaanvragen. Deze standaarden stellen gemeenten in staat gegevens over interacties tussen inwoners en ondernemers en de gemeente op gestandaardiseerde wijze registreren, bewerken en verwijderen. De drie (concept)standaarden samen noemen we de 'API-standaarden voor Klantinteracties'.

De drie API-standaarden voor Klantinteracties kennen een verschillende oorsprong. Met de API-standaarden voor Klanten en Contactmomenten 'verzelfstandigen' we in feite objecten uit de het [Informatiemodel Zaken (RGBZ)](https://www.gemmaonline.nl/index.php/RGBZ_2.0_in_ontwikkeling) en (op termijn) de [Zaken API-standaard](https://vng-realisatie.github.io/gemma-zaken/standaard/zaken/index). Op deze manier kunnen eenvoudiger buiten de context van zaken worden gebruikt. Daarbij geldt de volge
- 'klant' vervangt op termijn [betrokkene](https://www.gemmaonline.nl/index.php/Rgbz_2.0/doc/objecttype/betrokkene) waar betrokkenen die betrokkene
- Een contactmoment [klantcontact](https://www.gemmaonline.nl/index.php/Rgbz_2.0/doc/objecttype/klantcontact)
De reden hiervoor is dat gegevens over klanten en beschrijvingen van interacties tussen deze klanten

Productaanvragen heeft een andere reden

### Toegevoegde waarde voor gemeenten

- Er ontstaat een gemeentelijke kernregistratie 
- Lagere ontwikkelkosten van koppelingen op basis van de ZGW API's
- Lagere beheerkosten door backwards compatibiliteit (wijzigingen in de
  standaard leiden meestal niet tot aanpassingen in bestaande koppelingen)
- Voorkomen lock-in door echt uitwisselbare componenten
- Hogere kwaliteit van de standaard doordat deze in de praktijk en met
  medewerking van gemeenten en leveranciers is ontwikkeld. En ook door parallel
  aan de standaard een werkende referentie-implementatie te ontwikkelen
- Een herbruikbare, plug and play API waarmee in apps en applicaties de basale
  zaak(document) functionaliteiten consistent gebruikt kunnen worden

### Toegevoegde waarde voor leveranciers

- Lagere ontwikkelkosten van het koppelvlak
- Kunnen zich onderscheiden op onderdelen die burgers, bedrijven en medewerkers
  raken (i.p.v. te concurreren op infrastructuur)

### Toegevoegde waarde voor VNG Realisatie

- Beheer van de standaard is eenvoudiger doordat aanpassingen gemakkelijker
  zijn door te voeren
- Kwaliteitscontrole van koppelvlakken van leveranciers is eenvoudiger en
  daarmee goedkoper.
- Backwards compatibiliteit is eenvoudiger te behouden
