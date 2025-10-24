+++
date = '2024-05-16'
title = 'Automatisierte Datenbank-Migrationen mit Goose'
description = 'Von manuellen SQL-Skripten zu versionskontrollierten Datenbank-Migrationen'
technologies = ["MySQL", "MariaDB", "PowerShell", "SQL"]
+++

Für einen Kunden mit einem MySQL/MariaDB-Cluster implementierte ich ein modernes Migrationssystem, das manuelle Datenbankänderungen durch automatisierte, nachvollziehbare Migrationen ersetzt.

**Die Ausgangssituation**: Der Kunde betrieb vier Datenbanken auf zwei Servern (Produktiv- und Testumgebung). Strukturänderungen wurden manuell durch direktes Einspielen von SQL-Skripten vorgenommen – ohne systematische Versionskontrolle oder automatische Nachverfolgung. Um herauszufinden, welche Änderungen in welcher Datenbank bereits angewendet waren, musste der zuständige Mitarbeiter die Datenbankstruktur manuell prüfen. Dieser Prozess war fehleranfällig, zeitaufwändig und erschwerte die Synchronisation zwischen Test- und Produktivumgebung erheblich.

**Die Lösung**: Durch die Einführung von [Goose &nearr;](https://pressly.github.io/goose/) als Migrations-Framework weiß nun jede Datenbank selbst, welche Migrationen bereits angewendet wurden und welche noch ausstehen:

- **Versionierte Migrationen**: Alle Strukturänderungen werden als nummerierte SQL-Migrationsskripte verwaltet und versioniert
- **Automatische Statusverfolgung**: Goose protokolliert in der Datenbank selbst, welche Migrationen bereits durchgeführt wurden
- **Einheitliche Skriptbasis**: Test- und Produktivserver nutzen den gleichen Bestand an Migrationsskripten
- **Benutzerfreundliche Automatisierung**: PowerShell-Wrapper-Skripte ermöglichen die einfache Ausführung über die Kommandozeile – auch für nicht-technisches Personal

**Besonderer Fokus**: Damit die Mitarbeiter beim Kunden für das Einspielen der Updates keine tiefgreifenden technischen Kenntnisse besitzen müssen, wurden die PowerShell-Skripte bewusst so gestaltet, dass Datenbank-Updates mit einfachen Befehlen sicher und zuverlässig durchgeführt werden können.

Das neue System eliminiert manuelle Fehlerquellen, schafft vollständige Transparenz über den Zustand jeder Datenbank und ermöglicht schnelle, reproduzierbare Deployments – ohne dass tiefes Datenbank-Know-how erforderlich ist.
