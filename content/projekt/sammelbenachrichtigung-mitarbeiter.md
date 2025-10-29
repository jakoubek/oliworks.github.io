+++
date = '2022-01-01'
title = 'Effiziente Mitarbeiter-Kommunikation auf Knopfdruck'
description = 'Hunderte Mitarbeiter in Minuten informieren – per E-Mail oder SMS'
technologies = ['E-Mail', 'SMS', 'API', 'SAP SQL Anywhere', 'Xojo', 'Go']
contentQuality = 4
+++

Wie ein mittelständisches Unternehmen hunderte Mitarbeiter in Minuten statt Stunden erreicht – mit einem maßgeschneiderten Benachrichtigungssystem.

## Ausgangssituation

Das Unternehmen stand regelmäßig vor der Herausforderung, große Mitarbeitergruppen zeitkritisch informieren zu müssen – etwa bei Schichtänderungen, dringenden Betriebsmitteilungen oder Notfällen. Die manuelle Benachrichtigung per E-Mail oder Telefon band erhebliche Personalressourcen und war fehleranfällig.

## Die Herausforderung

- **Zeitdruck**: Hunderte Mitarbeiter mussten innerhalb kürzester Zeit erreicht werden
- **Zielgenaue Auswahl**: Nicht alle Mitarbeiter, sondern spezifische Gruppen nach Abteilung, Standort oder Funktion
- **Erreichbarkeit sicherstellen**: E-Mail genügt nicht immer – SMS als Fallback notwendig
- **Integration**: Mitarbeiterdaten lagen bereits in der bestehenden Warenwirtschaft vor

## Die Lösung

Ich entwickelte ein datenbankbasiertes Benachrichtigungssystem, das nahtlos an die vorhandene Unternehmenssoftware andockt:

### Benutzerfreundliche Bedienung

Über eine intuitive Anwendung können Mitarbeiter mit wenigen Klicks Zielgruppen auswählen – basierend auf den Strukturen aus der Warenwirtschaft. Eine Nachricht formulieren, Versandkanal wählen (E-Mail, SMS oder beides) – fertig.

### Intelligente Zustellung

Das System arbeitet mit einer Warteschlange: Benachrichtigungsaufträge werden in die Datenbank geschrieben und von einem Hintergrunddienst zuverlässig abgearbeitet. E-Mails gehen über die vorhandene Infrastruktur raus, SMS werden über einen professionellen Dienstleister versendet. Bei E-Mail-Zustellproblemen greift automatisch der SMS-Fallback.

### Eingesetzte Technologien

- **Datenbank**: SAP SQL Anywhere für zuverlässige Queue-Verarbeitung und Protokollierung
- **Backend-Entwicklung**: Go für den performanten Versand-Service
- **Integration**: REST-API-Anbindung an SMS-Dienstleister
- **Infrastruktur**: SMTP-Relay für E-Mail-Versand

### Das Ergebnis

- ⏱️ **Zeitersparnis**: Benachrichtigungen, die früher Stunden dauerten, sind in Minuten erledigt
- 🎯 **Treffsicherheit**: Nur relevante Mitarbeiter werden angesprochen
- ✅ **Zuverlässigkeit**: Automatische Fallback-Mechanismen garantieren Zustellung
- 📊 **Nachvollziehbarkeit**: Alle Benachrichtigungen werden protokolliert und sind nachweisbar
