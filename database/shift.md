---
description: Definition des Shift Models
---

# Shift

Das Shift Model dient zur Repräsentation einer geleisteten "Arbeitsschicht". Eine Schicht ist der Zeitraum zwischen
dem der User seine Arbeit begonnen und diese wieder beendet hat. Es können pro Tag mehrere Schichten erstellt
werden. Das Modell is t wie folgt definiert :

|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| started | DateTimeField() | Startzeit und Datum  |
| stopped | DateTimeField() | Endzeit und Datum  |
| contract| ForeignKey(to=Contract) | Relation zu einem Vertragseintrag |
| type    | CharField(choices=\["Shift", "Sick", "Vacation"\]) |    |
| note    | TextField() |    |
| tags    | TaggableManager() | Userdefinierte Tags zu dieser Schicht |
| created_at | DateTimeField(auto_now_add=True) | Timestamp wann der Eintrag erstellt wurde    |
| created_by | ForeignKey(to=User) | Eintrag wurde von diesem User erstellt   |
| modified_at | DateTimeField(auto_now=True) |  Timestamp an dem der Eintrag modifiziert wurde  |
| modified_by | ForeignKey(to=User) | User der den Eintrag modifiziert hat   |
| was_exported | BooleasnField(default=False) | Marker ob diese Schicht bereits über einen Reprot exportiert wurde |
|---------|-----------|--------|

Ein Eintrag in der Shifttabelle ist somit mit dem Nutzer, der sie speichert/gearbeitet hat, und zu dem jeweils gehörigen 
Vertrag verknüpft. Ferner stellt er eine zusammenhängende Arbeitszeit am Tag, jedoch nicht die insgesamt an diesem Tag 
gearbeitete Zeit dar.