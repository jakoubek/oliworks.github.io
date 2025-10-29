+++
date = '2018-01-01'
draft = false
title = 'Automatisierte Fakturierung und Forecasting-Schnittstelle'
description = 'Automatisierte Schnittstelle zwischen Warenwirtschaft und SAP für fehlerfreie Fakturierung und tagesaktuelle Forecasting-Daten. Zeitersparnis durch vollautomatischen Datenexport.'
technologies = ['Go', 'SAP SQL Anywhere', 'API']
contentQuality = 4
+++

## Die Herausforderung

Ein Unternehmen der Verteillogistik stand vor mehreren Herausforderungen beim Datenaustausch zwischen dem Warenwirtschaftssystem und SAP:

Die manuelle Übertragung von Auftrags- und Fakturadaten war zeitaufwendig und fehleranfällig. Mitarbeiter mussten regelmäßig Daten zwischen den Systemen transferieren, was zu Verzögerungen in der Rechnungsstellung führte. Gleichzeitig fehlte eine zeitnahe Datengrundlage für das Forecasting, da die Planungsdaten nicht aktuell genug waren.

Der Kunde benötigte eine Lösung, die sowohl die Fakturierung beschleunigt als auch eine verlässliche Basis für die Unternehmensplanung schafft.

## Die Lösung

Ich habe eine automatisierte Schnittstellenlösung konzipiert und entwickelt, die den Datenfluss zwischen Warenwirtschaft und SAP vollständig automatisiert:

Das System exportiert täglich die relevanten Auftragsdaten für das Forecasting und übermittelt diese automatisch an die SAP-Schnittstelle. Parallel dazu werden die abgeschlossenen Fakturadaten kontinuierlich übertragen, sodass die Rechnungserstellung direkt aus SAP heraus erfolgen kann. Eine wöchentliche Bereinigung storniert automatisch abgelaufene Aufträge und hält die Datenbestände aktuell.

Die Architektur wurde so konzipiert, dass sie zuverlässig im Hintergrund läuft und die Fehleranfälligkeit manueller Prozesse eliminiert.

## Das Ergebnis

Die Automatisierung brachte dem Kunden spürbare Verbesserungen:

- **Zeitersparnis**: Die manuelle Datenübertragung entfällt vollständig, Mitarbeiter können sich auf wertschöpfende Tätigkeiten konzentrieren.
- **Schnellere Fakturierung**: Rechnungen können zeitnah erstellt werden, da die Daten automatisch in SAP verfügbar sind.
- **Verbesserte Planungsgrundlage**: Das Forecasting basiert nun auf tagesaktuellen Daten, was fundiertere Geschäftsentscheidungen ermöglicht.
