+++
date = '2025-10-22T12:51:52+02:00'
title = 'FERAG-String erzeugen'
description = 'Wie Sie mit meinen Open-Source-Bibliotheken dynamisch TSL-Dateien für Ihre FERAG-Versandanlage erzeugen können'
technologies = ['FERAG-String', 'Go', 'Laravel', 'PHP', 'PostgreSQL']
+++

Für den Versand in Ihrer Druckereilogistik benötigen Sie einen FERAG-String zur Ansteuerung Ihrer FERAG-Versandanlage? Ich zeige Ihnen, wie leicht Sie mit Hilfe meiner Open-Source-Bibliothek **feragstring** selbst eine FERAG-String-Datei aus Ihren Logistikdaten erzeugen können.

Die Bibliothek zur Erzeugung eines FERAG-Strings ist für **Go** und **PHP** verfügbar. Außer Grundkenntnissen in Go oder PHP und Ihren produktionsrelevanten Daten benötigen Sie nichts, um sofort selbst einen FERAG-String zu erzeugen.

Sie können mit Hilfe dieser Bibliothek ein Programm erzeugen, das aus Ihren produktionsrelevanten Daten (z.B. aus einer CSV-Datei oder per direktem Zugriff auf eine Datenbank) einen FERAG-String erzeugt.

Diese Bibliothek wird erfolgreich bei mehreren Zeitungsverlagen zur Erzeugung von FERAG-String-Dateien eingesetzt. Dabei erfolgt der Einsatz – abhängig von der vorhandenen Architektur – sowohl innerhalb eines Go-Programms als auch als PHP-Anwendung. Es gibt Konstellationen, bei denen das Server-Programm direkt auf eine Datenbank oder API mit den zugrundeliegenden Logistikdaten zugreift und daraus dann die TSL-Datei erstellt. In einem anderen Fall wurde ein Standalone-Webserver (Laravel) aufgesetzt. Dieser holt von einem FTP-Server eine Excel-Datei mit den Logistikdaten und erzeugt daraus die TSL-Datei, die anschließend auf einen anderen FTP-Server geschrieben wird.

Bei allen Lösungen wurde Wert darauf gelegt, dass diese vollautomatisiert und zeitgesteuert ohne manuellen Eingriff arbeiten.

Ähnliche Projekte gibt es auch für Umgebungen, bei denen Versandförderanlagen von Sitma, Müller Martini oder Duplo genutzt werden. Dafür werden dann Dateien in einem entsprechenden Format erstellt (z.B. XML).
