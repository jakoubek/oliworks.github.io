+++
date = '2025-03-01'
title = 'Vornamencheck-API'
description = 'API zur automatisierten Bestimmung des Geschlechts zu einem Vornamen'
technologies = ['API']
+++

Der *Vornamencheck* ist eine kostenfrei verfügbare API, über die sich zu einem Vornamen das (mutmaßliche) Geschlecht ermitteln lässt.

Damit können Unternehmen ihre Adressdatenbanken prüfen. Nichts ist peinlicher, als wenn man bei Anschreiben die eigenen Kunden mit der offensichtlich falschen Anrede adressiert - und das nur, weil jemand bei der Anlage des Datensatzes das falsche Geschlecht ausgewählt hat. (Ja, es gibt Menschen, die sich nicht mit einem Geschlecht anreden lassen möchten &ndash; und das ist ok. Das ist aber nicht das Thema hier.)

Die Nutzung der API ist denkbar einfach: über einen simplen HTTP-GET-Request kann ein Vornamen abgeprüft werden:

```
GET https://vornamencheck.de/api/v1/names/gender?name=mary
```

Die Integration solcher Aufrufe lassen sich mit praktisch jeder Skript- oder Programmiersprache umsetzen.

Nähere Details kann man auf der Vornamencheck-Website unter 
[vornamencheck.de](https://vornamencheck.de/?ref=ow) sehen.
