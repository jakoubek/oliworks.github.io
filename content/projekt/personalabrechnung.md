+++
date = '2025-10-22T13:01:54+02:00'
title = 'Software für Personalabrechnung'
description = 'Individuelle Bruttolohnermittlung aus Warenwirtschaftsdaten'
technologies = ['SAP SQL Anywhere', 'Lazarus']
+++

Für ein Unternehmen aus dem Bereich der Medienlogistik wurde eine individuelle Software zur massenweisen Bruttolohnabrechnung einer umfangreichen Beschäftigtengruppe geschaffen. Aus der angebundenen Warenwirtschafts-Software werden die lohnrelevanten Daten ausgelesen und daraus Lohndaten erzeugt. Dabei werden zur Mindestlohnberechnung auch arbeitszeitabhängige Berechnungen berücksichtigt. Der fertige Datensatz wird dann zur tatsächlichen Nettolohnabrechnung an SAP übergeben.

Die Geschäftslogik wurde komplett innerhalb einer SQL Anywhere-Datenbank in Form von Stored Procedures umgesetzt. Zur vereinfachten Bedienung gibt es ein in Lazarus geschriebenes Frontendprogramm.
