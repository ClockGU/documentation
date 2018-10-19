---
description: Definition des Report Models
---

#Report


Das Report Model wird genutzt um den aktuellen Stand der gearbeiteten Zeit des Nutzers im Monat zu speichern.
Ferner dient es um am Ende des Monats einen Stundenzettel einfacher zu erstellen. Demnach wird jeden Monat ein neuer
Report eintrag erstellt.


|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| month_year | DateField() | Monat/Jahr für den/das der Report gilt |
|hours    | DurationFiled() | Dauer der bereits gearbeiteten Zeit in diesem Monat |
| contract| ForeignKey(to=Contract) | Relation zu einem Vertragseintrag |
| created_at | DateTimeField(auto_now_add=True) |    |
| created_by | ForeignKey(to=User) |    |
| modified_at | DateTimeField(auto_now=True) |    |
| modified_by | ForeignKey(to=User) |    |
|---------|-----------|--------|