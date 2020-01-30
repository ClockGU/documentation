---
description: Definition des Report Models
---

# Report Model

Das _Report-Model_ wird genutzt, um den aktuellen Stand der gearbeiteten Zeit des Nutzers im Monat zu speichern. Ferner dient es dazu, am Ende des Monats einen Erfassungsbogen \("Stundenzettel"\) zu erstellen. Demnach wird jeden Monat ein neuer _Report-Eintrag_ erstellt.

| Feldname | Feld Type | Nutzung |
| :--- | :--- | :--- |
| id | UUIDField\(primary\_key= True, default=uuid.uuid4, editable=False, unique=True\) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt |
| user | ForeignKey\(to=User\) | Relation zu einem Usereintrag |
| month\_year | DateField\(\) | Monat eines Jahres, auf den sich der Report bezieht |
| hours | DurationField\(\) | Dauer der bereits gearbeiteten Zeit in diesem Monat |
| contract | ForeignKey\(to=Contract\) | Relation zu einem Vertragseintrag |
| created\_at | DateTimeField\(auto\_now\_add=True\) | Timestamp \(Zeitpunkt\), an dem der Eintrag erstellt wurde |
| created\_by | ForeignKey\(to=User\) | User der den Eintrag erstellt hat |
| modified\_at | DateTimeField\(auto\_now=True\) | Timestamp, an dem der Eintrag zuletzt modifiziert wurde |
| modified\_by | ForeignKey\(to=User\) | User, der den Eintrag zuletzt modifiziert hat |
| --------- | ----------- | -------- |

