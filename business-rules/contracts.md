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
* ... Verträge zu erstellen, welche nicht am 1. oder 16. eines Monats beginnen.
* ... Verträge zu erstellen, welche nicht am 15. oder Letzten eines Monates enden.
* ... Verträge zu erstellen, deren `hours` &lt;= 0 sind.
* ... Verträge zu erstellen, deren `month_start_clocking` _nicht_ im Interval zwischen `start_date` und `end_date` liegt.
* ... Verträge zu erstellen, deren `month_start_clocking` _nicht_ der 1. eines Monats ist.
Einem Nutzer ist es ferner _nicht_ möglich Verträge in der Zukunft zu erstellen, falls ...

* `month_start_clocking` _nicht_ der 1. des `start_date` Monats/Jahres ist.
* `start_carry_over` _nicht_ 0 ist.[^1] 


[^1] : Auch wenn es sich um einen direkten Folgevertrag handelt darf kein Übertrag mitgenommen werden.


