---
description: Übersicht zur Datenbank
---

# Einleitendes

Die Datenbank des Projekts basiert auf [PostgreSQL 9.4+], welches nativ von Django unterstützt wird. Innerhalb des Codes wird die Datenbank von Django verwaltet weshalb keine SQL Statements in reiner Form verwendet werden müssen.

Im Folgenden Kapitel werden alle implementierten Datenbanktabellen (im folgenden *Model/s* genannt) definiert. Hier werden Modelnamen, Feldnamen, gespeicherte Datentypen und Relationen zu anderen Models dargelegt. Falls der Nutzen des jeweiligen Models nicht direkt ersichtlich ist wird dieser ferner erläutert.

Die Models spiegeln den jeweiligen *Serializer* wider, so dass die grundlegenden Serializer nicht weiter erläutert werden.
Serializer, die eine Abstraktion der Models sind oder sich nicht direkt aus einem Model ergben werden im Kapitel *Serializer* definiert und erläutert.

#### Anmerkungen:
* *Django* ist ein Open-Source Web-Framework, das die Anfragen zwischen Webbrowser und Datenbank verarbeitet. Es nutzt die Programmiersprache *Python* (https://www.djangoproject.com/).
* *SQL* ist eine Datenbanksprache; PostgreSQL (https://www.postgresql.org/) ist ein dazu passendes Datenbankmanagementsystem
* *Serializer* übersetzen die Datenstrukturen der Datenbank in ein Datenobjekt in JSON-Notation, welches die jeweiligen über die Benutzeroberfläche angefragten Informationen enthält. 
