+++
date = '2020-11-25'
title = 'DatesAPI'
description = 'Ein kostenfrei nutzbarer Webservice, der Datumswerte bereitstellt und einfach in Make oder Zapier eingebunden werden kann'
technologies = ['Automatisierung', 'Go', 'API']
contentQuality = 2
+++

**DatesAPI** ist ein in Go geschriebener Webservice, der Informationen zu "Datums" bereitstellt. Ich habe diesen Dienst aufgesetzt, weil Datumsmanipulationen in den üblichen Automatisierungsplattformen (Zapier, Make, ...) sehr umständlich zu realisieren sind. Dies gilt umso mehr, wenn man Datumsangaben (z.B. Monatsnamen) auf deutsch weiterverwenden möchte.

Im konkreten Fall hatte ich mehrere *Szenarien* (Make bzw. Integromat), die zeitgesteuert gegen Ende des Monats laufen und die in meinem **Ticketsystem** (Kanboard) neue Tickets für den nächsten Monat anlegen. Diese Tickets heißen dann z.B. *Monatsabschluss Juli 2024*. Die dynamische, weil jeden Monat wechselnde Erzeugung des Strings "Juli 2024" (insbesondere mit nicht-englischem Monatsnamen) war nur aufwändig möglich und hätte für jedes Szenario wieder neu angelegt werden müssen.

Statt dessen greife ich aus diesen Automatisierungsplattformen direkt über das eingebaute HTTP-Modul auf meinen Datums-Webservice zu und hole mir von dort die notwendigen Angaben.

```
GET https://api.datesapi.net/today
GET https://api.datesapi.net/tomorrow
GET https://api.datesapi.net/next-month?lang=de
```

Die Landing-Page für den Dienst ist über [datesapi.net](https://datesapi.net/?ref=ow) zu erreichen. Anfragen können über Curl oder Skripte direkt an die Endpunkte unter **api.datesapi.net** gesendet werden, z.B. für das heutige Datum (https://api.datesapi.net/today) oder den nächsten Monat (https://api.datesapi.net/next-month?lang=de).
