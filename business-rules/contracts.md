---
description: Business Rules für das Contract Model
---

# Contract Model

Für das _Contract_-Model gelten die im Folgenden aufgelisteten Einschränkungen:

Einem Nutzer ist es nicht möglich, ...

* ... auf Verträge zuzugreifen, die _nicht_ ihm gehören.
* ... Verträge zu bearbeiten, die _nicht_ ihm gehören.
* ... Verträge zu löschen, die _nicht_ ihm gehören.
* ... Verträge zu löschen sofern _bereits_ _Report_-Objekte dazu existieren.
* ... Verträge zu bearbeiten sofern _bereits_ _Shift_-Objekte dazu existieren.
* ... Verträge zu erstellen, die _vor_ dem aktuellen Monat enden.
* ... Verträge zu erstellen, welche nicht am 1. oder 15. eines Monats beginnen.
* ... Verträge zu erstellen, welche nicht am 14. oder Letzten eines Monates enden.
* ... Verträge zu erstellen, deren `hours` &lt;= 0 sind.

