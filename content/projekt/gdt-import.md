+++
date = '2025-07-01'
title = 'GDT-Importtool für digitale Patientenaufnahme'
description = 'Automatisierte Integration von Patient-Intake-Systemen in Praxisverwaltungssoftware'
technologies = ['Go', 'PostgreSQL', 'GDT-Dateiformat-Parsing']
+++

Für einen Kunden aus dem Gesundheitswesen entwickelte ich ein Importtool, das moderne digitale Patientenaufnahme-Lösungen nahtlos mit bestehenden Praxisverwaltungssystemen verbindet.

**Die Herausforderung**: Viele Arztpraxen setzen auf digitale Patient-Intake-Tools (wie z.B. IDANA), um die Erstaufnahme zu modernisieren. Patienten erfassen ihre Stammdaten, Anamnese und Symptome bequem über Tablets im Wartezimmer. Diese modernen Lösungen nutzen den GDT-Standard (Geräte-Daten-Träger) – ein in Deutschland etabliertes Dateiformat für den Austausch von Patientendaten – um die erfassten Informationen an das Praxisverwaltungssystem (PVS) zu übergeben.

**Die Lösung**: Das entwickelte Tool automatisiert die vollständige Integration zwischen Patient-Intake-System und Praxisverwaltungssoftware:

- **Datenerfassung**: GDT-Dateien werden zusammen mit den vom Patienten ausgefüllten PDF-Fragebögen aus dem Importverzeichnis abgeholt
- **Patientenabgleich**: Anhand der Patientennummer aus der GDT-Datei erfolgt die eindeutige Zuordnung zum Patienten im Praxisverwaltungssystem
- **Datenbankintegration**: Direkter Zugriff auf die PostgreSQL-Datenbank des PVS ermöglicht das sichere Auslesen der Patientenstammdaten
- **Dokumentenverwaltung**: Die ausgefüllten PDF-Formulare werden automatisch in den patientenspezifischen Ablageordner sortiert
- **Audit-Trail**: Jeder Importvorgang wird in der elektronischen Patientenakte protokolliert – für vollständige Nachvollziehbarkeit

Das Tool ermöglicht Praxen, moderne digitale Patientenaufnahme-Systeme zu nutzen, ohne auf manuelle Datenübertragung oder Medienbrüche angewiesen zu sein. Die Patientendaten fließen automatisch vom Tablet in die Praxissoftware – sicher, fehlerfrei und dokumentiert.
