---
description: Business Rules für das Contract Model
---

# Contract Model

Für das *Contract*-Model gelten die im Folgenden aufgelisteten Einschränkungen:

Einem Nutzer ist es nicht möglich, ...

* ... auf Verträge zuzugreifen, die *nicht* ihm gehören.
* ... Verträge zu bearbeiten, die *nicht* ihm gehören.
* ... Verträge zu löschen, die *nicht* ihm gehören.
* ... Verträge zu löschen sofern *bereits* *Report*-Objekte dazu existieren.
* ... Verträge zu bearbeiten sofern *bereits* *Shift*-Objekte dazu existieren.
* ... Verträge zu erstellen, die *vor* dem aktuellen Monat enden.
* ... Verträge zu erstellen, welche nicht am 1. oder 15. eines Monats beginnen.
* ... Verträge zu erstellen, welche nicht am 14. oder Letzten eines Monates enden.
* ... Verträge zu erstellen, deren `hours` <= 0 sind.

