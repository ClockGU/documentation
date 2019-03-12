---
description: Definition des Report Models
---

# Report


Das *Report*-Model wird genutzt, um den aktuellen Stand der gearbeiteten Zeit des Nutzers im Monat zu speichern.
Ferner dient es dazu, am Ende des Monats einen Erfassungsbogen ("Stundenzettel") zu erstellen. Demnach wird jeden Monat ein neuer
*Report*-Eintrag erstellt.


|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True, default=uuid.uuid4, editable=False, unique=True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| month_year | DateField() | Monat eines Jahres, auf den sich der Report bezieht |
|hours    | DurationFiled() | Dauer der bereits gearbeiteten Zeit in diesem Monat |
| contract| ForeignKey(to=Contract) | Relation zu einem Vertragseintrag |
| created_at | DateTimeField(auto_now_add=True) | Timestamp (Zeitpunkt), an dem der Eintrag erstellt wurde   |
| created_by | ForeignKey(to=User) |  User der den Eintrag erstellt hat |
| modified_at | DateTimeField(auto_now=True) |  Timestamp, an dem der Eintrag zuletzt modifiziert wurde  |
| modified_by | ForeignKey(to=User) |  User, der den Eintrag zuletzt modifiziert hat  |
|---------|-----------|--------|
