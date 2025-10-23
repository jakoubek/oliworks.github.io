+++
date = '2024-05-16'
title = 'Datenbank-Migrationen'
description = 'Einführung eines Datenbank-Migrationstools zur Weiterentwicklung von Datenbank-Strukturen'
technologies = ["MySQL", "MariaDB", "PowerShell", "SQL"]
+++

Für ein bestehendes MySQL-/MariaDB-Datenbank-Cluster wurde die Weiterentwicklung der Datenbankstrukturen auf ein zeitgemäßes Migrationstool umgestellt.

Davor wurden Änderungen einfach durch Einspielen des richtigen SQL-Skripts auf der Datenbank vorgenommen. Dabei musste über eine externe Dokumentation oder die manuelle Sichtung der Datenbank-Strukturen ermittelt werden, welche Strukturänderungen in welcher Datenbank noch fehlen.

Durch die Einführung eines Migrationstools (hier: [goose](https://pressly.github.io/goose/)) ist sichergestellt, dass die jeweilige Datenbank selbst weiß, welche Änderungen noch fehlen. Über einfache PowerShell-Skripte können alle Datenbanken - sowohl auf dem Test- als auch auf dem Produktivserver - gezielt aktualisiert werden. Dabei bedienen sich diese Skripte für alle Server/Umgebungen aus dem gleichen Bestand an SQL-Migrationsskripten.

Die PowerShell-Skripte wurden gezielt so bereitgestellt, dass nicht-technisches Projektpersonal diese nutzen kann.
