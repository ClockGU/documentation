---
description: Definition des Shift Models
---

# Shift Model

Das Shift Model dient zur Repräsentation einer geleisteten "Arbeitsschicht". Eine Schicht ist der Zeitraum zwischen Beginn der Arbeit und dessen Ende. Es können pro Tag mehrere Schichten erstellt werden. Das Modell ist wie folgt definiert :

| Feldname | Feld Type | Nutzung |
| :--- | :--- | :--- |
| id | UUIDField\(primary\_key= True, , default=uuid.uuid4, editable=False, unique=True\) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt |
| user | ForeignKey\(to=User\) | Relation zu einem Usereintrag |
| started | DateTimeField\(\) | Startzeit und Datum |
| stopped | DateTimeField\(\) | Endzeit und Datum |
| contract | ForeignKey\(to=Contract\) | Relation zu einem Vertragseintrag |
| type | CharField\(choices=\["Shift", "Sick", "Vacation"\]\) | Art der Schicht \(normal, krank, Urlaub\) |
| note | TextField\(\) | Eine vom Benutzer eingegebene Bemerkung \(optional\) |
| tags | TaggableManager\(\) | Userdefinierte Tags zu dieser Schicht \(zur Strukturierung der Aufgaben\) |
| was\_reviewed | BooleanField\(default=True\) | Status, ob eine Schicht geplant ist |
| was\_exported | BooleanField\(default=False\) | Status, ob eine Schicht bereits über einen _Report_ exportiert wurde |
| created\_at | DateTimeField\(auto\_now\_add=True\) | Timestamp \(Zeitpunkt\), wann der Eintrag erstellt wurde |
| created\_by | ForeignKey\(to=User\) | User, von dem der Eintrag erstellt wurde |
| modified\_at | DateTimeField\(auto\_now=True\) | Timestamp, an dem der Eintrag zuletzt modifiziert wurde |
| modified\_by | ForeignKey\(to=User\) | User, der den Eintrag zuletzt modifiziert hat |
| --------- | ----------- | -------- |

Ein Eintrag in der _Shift_-Tabelle ist mit dem Nutzer, der sie speichert bzw. der gearbeitet hat und zum jeweiligen Vertrag verknüpft. Ferner stellt er eine _zusammenhängende_ Arbeitszeit am Tag, jedoch nicht die insgesamt an diesem Tag gearbeitete Zeit dar. Diese kann sich aus mehreren Schichten zusammensetzen.

## Bemerkung:

Das Feld `was_reviewed` definiert, ob eine Schicht als _geplant_ gilt. Eine geplante Schicht liegt mit Start- und Endzeit/datum in der Zukunft. Bei gestochenen bzw. manuell eingetragenen Schichten \(Start- und Endzeit/-datum liegen in der Vergangenheit\) ist der Wert des Feldes automatisch auf `True` gesetzt.

Mehr dazu in den [Business Rules](https://github.com/ClockGU/documentation/tree/d9017ef23486145bd22fcaf7804dab7e3ad8c5e5/database/business-rules/shifts.md).

