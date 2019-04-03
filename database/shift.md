---
description: Definition des Shift Models
---

# Shift

Das Shift Model dient zur Repräsentation einer geleisteten "Arbeitsschicht". Eine Schicht ist der Zeitraum zwischen Beginn der Arbeit und dessen Ende. Es können pro Tag mehrere Schichten erstellt werden. Das Modell ist wie folgt definiert :

|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True, , default=uuid.uuid4, editable=False, unique=True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| started | DateTimeField() | Startzeit und Datum  |
| stopped | DateTimeField() | Endzeit und Datum  |
| contract| ForeignKey(to=Contract) | Relation zu einem Vertragseintrag |
| type    | CharField(choices=\["Shift", "Sick", "Vacation"\]) |  Art der Schicht (normal, krank, Urlaub)  |
| note    | TextField() |  Eine vom Benutzer eingegebene Bemerkung (optional)  |
| tags    | TaggableManager() | Userdefinierte Tags zu dieser Schicht (zur Strukturierung der Aufgaben) |
| was_reviewed | BooleanField(default=True) | Status, ob eine Schicht geplant ist|
| was_exported | BooleanField(default=False) | Status, ob eine Schicht bereits über einen *Report* exportiert wurde |
| created_at | DateTimeField(auto_now_add=True) | Timestamp (Zeitpunkt), wann der Eintrag erstellt wurde    |
| created_by | ForeignKey(to=User) | User, von dem der Eintrag erstellt wurde |
| modified_at | DateTimeField(auto_now=True) |  Timestamp, an dem der Eintrag zuletzt modifiziert wurde  |
| modified_by | ForeignKey(to=User) | User, der den Eintrag zuletzt modifiziert hat   |
|---------|-----------|--------|

Ein Eintrag in der *Shift*-Tabelle ist mit dem Nutzer, der sie speichert bzw. der gearbeitet hat und zum jeweiligen Vertrag verknüpft. Ferner stellt er eine *zusammenhängende* Arbeitszeit am Tag, jedoch nicht die insgesamt an diesem Tag gearbeitete Zeit dar. Diese kann sich aus mehreren Schichten zusammensetzen.

#### Bemerkung:

Das Feld `was_reviewed` definiert, ob eine Schicht als *geplant* gilt. Eine geplante Schicht liegt mit Start- und Endzeit/datum in der Zukunft. Bei gestochenen bzw. manuell eingetragenen Schichten (Start- und Endzeit/-datum liegen in der Vergangenheit) ist der Wert des Feldes automatisch auf `True` gesetzt.

Mehr dazu in den [Business Rules](business-rules/shifts.md).
