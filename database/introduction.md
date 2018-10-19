---
description: Übersicht zur Datenbank
---

# Einleitendes

Die Datenbank des Projektes basiert auf (PostgreSQL 9.4+)[https://www.postgresql.org/], welches nativ von Dajngo
unterstützt wird. Innerhalb des Codes wird die Datenbank von Django verwaltet weshalb keine SQL statements in roher form
verwendet werden. Im Folgenden Kapitel werden alle implementierten Datenbanktabellen (in folgenden Models/s genannt)
definiert. Hier werden Modelnamen, Feldernamen, gespeicherte Datentypen und Relationen zu anderen Models dargelegt. 

Falls der Nutzen des jeweiligen Models nicht direkt ersichtlich ist wird dieser ferner erläutert.

Die Models spiegeln direkt den jeweiligen Seralizer (Antwort JSON Objekt der API) wieder so dass die grundlegenden
Serializer nicht weiter erläutert werden. Serializer die eine Abstraktion der Models sind oder sich nicht direkt 
aus einem Model ergben werden im Kapitel *Serializer* definiert und erläutert.