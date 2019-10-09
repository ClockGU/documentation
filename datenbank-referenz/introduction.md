---
description: Übersicht zur Datenbank
---

# Einleitendes

Die Datenbank des Projekts basiert auf \[PostgreSQL 9.4+\], welches nativ von Django unterstützt wird. Innerhalb des Codes wird die Datenbank von Django verwaltet, weshalb keine SQL Statements in reiner Form verwendet werden müssen.

Im Folgenden Kapitel werden alle implementierten Datenbanktabellen \(im folgenden _Model/s_ genannt\) definiert. Hier werden Modelnamen, Feldnamen, gespeicherte Datentypen und Relationen zu anderen Models dargelegt. Falls der Nutzen des jeweiligen Models nicht direkt ersichtlich ist, wird dieser ferner erläutert.

Die Models spiegeln den jeweiligen _Serializer_ wieder, sodass die grundlegenden Serializer nicht weiter erläutert werden. Serializer, die eine Abstraktion der Models sind oder sich nicht direkt aus einem Model ergeben werden im Kapitel _Serializer_ definiert und erläutert.

## Anmerkungen:

* _Django_ ist ein Open-Source Web-Framework, das die Anfragen zwischen Webbrowser und Datenbank verarbeitet. Es nutzt die Programmiersprache _Python_ \([https://www.djangoproject.com/](https://www.djangoproject.com/)\).
* _SQL_ ist eine Datenbanksprache; PostgreSQL \([https://www.postgresql.org/](https://www.postgresql.org/)\) ist ein dazu passendes Datenbankmanagementsystem
* _Serializer_ übersetzen die Datenstrukturen der Datenbank in ein Datenobjekt in JSON-Notation, welches die jeweiligen über die Benutzeroberfläche angefragten Informationen enthält. 

