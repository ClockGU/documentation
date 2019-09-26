---
description: Definition des Contract Models
---

# Contract Model

Das _Contract-Model_ stellt einen Vertrag eines Users dar. Ein User kann gemäß Vorgaben mehrere Verträge haben, für die jeweils unterschiedlich viele Stunden Arbeitszeit zu leisten sind. Das Model ist wie folgt definiert:

| Feldname | Feld Type | Nutzung |
| :--- | :--- | :--- |
| id | UUIDField\(primary\_key= True, default=uuid.uuid4, editable=False, unique=True\) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation eines Users in der Datenbank benutzt |
| user | ForeignKey\(to=User\) | Relation zu einem Usereintrag |
| name | CharField\(\) | Userdefinierter Name des Vertrags |
| hours | FloatField\(\) | Anzahl der monatlich zu leistenden Arbeitszeit in Minuten |
| start\_date | DateField\(\) | Vertragsbeginn |
| end\_date | DateField\(\) | Vertragsende |
| created\_at | DateTimeField\(auto\_now\_add=True\) | Timestamp \(Zeitpunkt\), an dem der Eintrag erstellt wurde |
| created\_by | ForeignKey\(to=User\) | User, der den Eintrag erstellt hat |
| modified\_at | DateTimeField\(auto\_now=True\) | Timestamp, an dem der Eintrag zuletzt verändert wurde |
| modified\_by | ForeignKey\(to=User\) | User, der den Eintrag zuletzt modifiziert hat |
| --------- | ----------- | -------- |

