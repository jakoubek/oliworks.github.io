+++
date = '2022-01-01'
title = 'Sammelbenachrichtigung'
description = 'Automatisierter Sammelversand von E-Mails und SMS'
technologies = ['E-Mail', 'SMS', 'API', 'SAP SQL Anywhere', 'Xojo', 'Go']
+++

Für ein Unternehmen wurde die Möglichkeit geschaffen, zeitsparend große Mitarbeitergruppen benachrichtigen zu können.

Dazu können über ein Frontendprogramm gezielt Empfängergruppen ausgewählt werden und eine Benachrichtigung hinterlegt werden. Die Definition der Empfängergruppen wird dabei über Strukturen aus der lokalen Warenwirtschaftsanwendung definiert. Die Benachrichtigung erfolgt dann wahlweise per E-Mail, SMS, E-Mail und SMS oder E-Mail und ersatzweise SMS.

Die erzeugten Benachrichtigungsaufträge werden in eine Datenbank-Queue geschrieben und regelmäßig von einem Serverprogramm verarbeitet. Dieses versendet die E-Mails über ein lokales SMTP-Relay. Die SMS werden an die API eines SMS-Dienstleisters gesendet.
