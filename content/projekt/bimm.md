+++
date = '2025-10-01'
draft = true
title = 'BIMM - Brustimplantate-Meldemodul'
description = ''
technologies = ['Go', 'PostgreSQL', 'API', 'Telematik-Infrastruktur']
contentQuality = 1
+++

BIMM (Brustimplantate-Meldemodul) ist ein in Go geschriebener Webserver mit PostgreSQL-Datenbank.

Die Patientendaten werden direkt aus der PostgreSQL-Datenbank von Pixelmedics gelesen.

Über BIMM kann eine Arztpraxis Brustimplantate erfassen und daraus Meldungen an die Schnittstelle des Implantateregisters des Bundesgesundheitsministeriums erzeugen.

Hintergrund ist, dass mittlerweile Implantationen (Brust, Herzklappen, Hüfte, Knie) an das Implantatregister gemeldet werden müssen.

Bis Ende 2026 stellt das Bundesgesundheitsministerium noch die Webanwendung "IRMA" bereit, über die Arztpraxen Implantationen melden können. Dies ist aber nur eine Übergangslösung. Langfristig müssen die Arztpraxen über gezielte Praxisverwaltungssoftwares diese Meldungen vornehmen.

Der Zugriff auf die Implantateregister-API erfolgt abgesichert innerhalb der Telematik-Infrastruktur.
