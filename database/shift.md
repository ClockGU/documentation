---
description: Definition des Shift Models
---

# Shift

Das Shift Model dient zur Repräsentation einer geleisteten "Arbeitsschicht". Eine Schicht ist der Zeitraum zwischen
dem der User seine Arbeit begonnen hat und diese wieder beendet hat. Es können pro Tag mehrere Schichten erstellt
werden. Das Modell is t wie folgt definiert :

|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| started | DateTimeField() |    |
| stopped | DateTimeField() |    |
| contract| ForeignKey(to=Contract) | Relation zu einem Vertragseintrag |
| type    | CharField(choices=\["Shift", "Sick", "Vacation"\]) |    |
| note    | TextField() |    |
| tags    | TaggableManager() | Userdefinierte Tags zu dieser Schicht |
| created_at | DateTimeField(auto_now_add=True) |    |
| created_by | ForeignKey(to=User) |    |
| modified_at | DateTimeField(auto_now=True) |    |
| modified_by | ForeignKey(to=User) |    |
|---------|-----------|--------|

Ein Eintrag in der Shifttabelle ist somit mit dem Nutzer, der sie speichert/gearbeitet hat, und zu dem jeweils gehörigen 
Vertrag verknüpft. Ferner stellt er eine zusammenhängende Arbeitszeit am Tag, jedoch nicht die insgesamt an diesem Tag 
gearbeitete Zeit dar.