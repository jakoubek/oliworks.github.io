+++
date = '2023-12-31'
title = 'Automatisierte Versandsteuerung für FERAG-Anlagen'
description = 'Automatische Erzeugung von FERAG-Strings aus bestehenden Logistiksystemen. Integration in Ihre Infrastruktur für fehlerfreie, vollautomatisierte Versandsteuerung ohne manuelle Eingriffe.'
technologies = ['FERAG-String', 'Go', 'Laravel', 'PHP', 'PostgreSQL', 'PDF']
contentQuality = 4
+++

## Die Herausforderung

Nach der Ablösung einer älteren Software fehlte Unternehmen eine zentrale Komponente ihrer Produktionskette. Sie benötigten eine Möglichkeit, aus ihren Logistik- und Auftragsdaten automatisch Steuerdateien (FERAG-Strings) für ihre Versandanlagen zu erzeugen. Eine manuelle Erstellung dieser hochkomplexen Dateien ist praktisch nicht möglich. Die bestehenden Logistiksysteme lieferten jedoch keine FERAG-Ausgabe.

Die Herausforderung lag darin, eine nahtlose Integration in die vorhandene IT-Infrastruktur zu schaffen. Dabei musste die Lösung mit unterschiedlichen Datenquellen arbeiten können.

## Die Lösung

Ich entwickelte für mehrere Kunden individuelle Integrationslösungen zur automatisierten Erzeugung von FERAG-Steuerdateien. Der Fokus lag auf der Analyse der bestehenden Systemarchitektur und der Konzeption einer passenden Integrationsstrategie.

**Unterschiedliche Architekturen erforderten unterschiedliche Ansätze:**

Bei einem Kunden erfolgt der direkte Zugriff auf die Datenbank mit den Logistikdaten. Das System erzeugt daraus automatisch die benötigten TSL-Dateien. Ein anderer Kunde nutzt eine API-basierte Anbindung an sein Logistiksystem.

In einem weiteren Fall wurde ein eigenständiger Webserver konzipiert. Dieser liest Excel-Dateien mit Logistikdaten von einem FTP-Server ein. Er erzeugt daraus die Steuerdateien und legt diese auf einem anderen FTP-Server ab. Diese Architektur ermöglichte die Integration ohne Eingriffe in bestehende Systeme.

**Wichtig bei allen Lösungen:** Die Systeme arbeiten vollautomatisiert und zeitgesteuert. Es sind keine manuellen Eingriffe erforderlich.

Für die technische Umsetzung nutze ich eine selbst entwickelte Open-Source-Bibliothek. Sie ist für Go und PHP verfügbar und ermöglicht flexible Anpassungen an kundenspezifische Anforderungen.

## Das Ergebnis

Die Kunden profitieren von einer **vollautomatischen Erzeugung** der Steuerdateien ohne manuelle Eingriffe. Dies führt zu deutlicher **Zeitersparnis** im Tagesgeschäft.

Die automatisierte Erzeugung reduziert Fehler drastisch. Die Produktionsprozesse laufen **zuverlässiger** ab.

Die Integration in bestehende Infrastrukturen (Datenbanken, APIs, FTP-Server) erfolgte nahtlos. Bestehende Systeme konnten weitergenutzt werden.

---

**Ähnliche Lösungen** entwickele ich auch für andere Versandförderanlagen wie Sitma, Müller Martini oder Duplo. Je nach Anlage werden dabei unterschiedliche Dateiformate erzeugt (z.B. XML-basierte Formate).
