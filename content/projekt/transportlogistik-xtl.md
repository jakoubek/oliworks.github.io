+++
date = '2023-11-01'
title = 'Transportlogistik XTL'
description = 'Automatisierte Tourenoptimierung durch Integration von Warenwirtschaft und Transportlogistik-System'
technologies = ['API', 'Go', 'SAP SQL Anywhere']
+++

## Die Herausforderung

Ein Logistik-Unternehmen stand vor mehreren Herausforderungen in der täglichen Tourenplanung: Es gab keine automatisierte Tourenoptimierung – die Reihenfolge der Stopps wurde manuell festgelegt, was weder Zeit noch Kosten optimierte. Die Fahrer arbeiteten mit ausgedruckten Tourenlisten auf Papier, wodurch zusätzlicher Verwaltungsaufwand entstand und Statusaktualisierungen in Echtzeit nicht möglich waren.

Das Unternehmen wollte die Transportlogistik-SaaS-Lösung [XTL](https://www.xtl-gmbh.de/) nutzen, um von deren Tourenoptimierungs-Algorithmen und Fahrer-App zu profitieren. Die zentrale Frage war: Wie lässt sich XTL nahtlos in die bestehende Warenwirtschaft integrieren, sodass alle Systeme optimal zusammenspielen?

## Die Lösung

In enger Zusammenarbeit wurde eine bidirektionale Integration zwischen Warenwirtschaftssystem und XTL konzipiert und umgesetzt. Dabei lag der Fokus auf einer robusten Architektur, die zuverlässige Datensynchronisation gewährleistet:

Die Transportaufträge werden automatisch aus der Warenwirtschaft an die XTL-API übertragen. Dort optimiert XTL die Tourenreihenfolge nach Zeit- und Kostenkriterien. Die optimierte Reihenfolge fließt zurück ins Warenwirtschaftssystem, wo sie für die weitere Abwicklung zur Verfügung steht. Gleichzeitig nutzen die Fahrer die XTL-App, um jeden Abladepunkt digital abzuhaken – der Status wird in Echtzeit ins System übertragen.

Die Architekturentscheidungen stellten sicher, dass die Integration auch bei hohem Auftragsvolumen stabil funktioniert und beide Systeme konsistent bleiben.

## Das Ergebnis

Durch die automatisierte Tourenoptimierung konnte das Unternehmen Transportkosten messbar senken – kürzere Wege bedeuten weniger Kraftstoffverbrauch und Zeitaufwand. Die Automatisierung der Datenübertragung spart täglich administrative Zeit ein, die vorher für manuelle Planung und Übertragung aufgewendet werden musste.

Der Verzicht auf papierbasierte Tourenlisten reduziert nicht nur Druckkosten, sondern ermöglicht auch eine durchgängig digitale Prozesskette mit Echtzeit-Transparenz über den Lieferstatus.
