+++
date = '2018-04-30'
title = 'Versandpapierdruck'
description = 'Massenweises Erzeugen von PDF-Papieren aus einer Warenwirtschaft'
technologies = ['SAP SQL Anywhere', 'Xojo', 'Go', 'PDF']
+++

Für ein Unternehmen aus dem Bereich Medienlogistik wurde die Möglichkeit geschaffen, auf Basis von Auftragsdaten in der Warenwirtschafts-Software wöchentlich PDF-Versandpapiere massenweise erzeugen zu können.

Damit war es möglich, dass das Unternehmen seine Versandpapiere für verschiedene Adressaten gezielt anpassen kann - ohne dafür eine aufwändige in den Kern der von außen gelieferten Warenwirtschafts-Anwendung vornehmen zu müssen.

Dabei werden die Auftragsdaten zu einem gegeben Zeitpunkt festgeschrieben. Die Nutzer greifen dann über ein Frontend-Programm auf diese Daten zu. Es können dann gezielt alle oder Teile der zum Druck verfügbaren Datensätze als PDF-Dokument ausgegeben werden. Dabei erfolgt direkt die Ablage der PDFs in einer sinnvollen Verzeichnisstruktur sowie der Druck auf einem zum jeweiligen PDF-Typ passenden Drucker.

Bei einer späteren Fortentwicklung dieser Anwendung wurde dann ein Kommandozeilen-Programm für den automatisierten Einsatz auf einem Server geschaffen. Dieses Programm verantwortet mittlerweile die Festschreibung der Auftragsdaten und die automatisierte Erzeugung der PDF-Dateien völlig autonom und zeitgesteuert.
Diese Lösung führt noch einmal zu einer erheblichen Zeitersparnis.
