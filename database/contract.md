---
description: Definition des Contract Models
---

# Contract

Das Contract Model stellt einen Vertrag eines Users dar. Ein User kann gemäß Vorgaben mehrere Verträge haben für die
jeweils unterschiedlich viele STunden Arbeitszeit zu leisten sind. Das Model ist wie folgt definiert:

|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation eines Users in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| name    | CharField()  | Userdefinierter Name des Vertrags |
| hours   | FloatField() | Anzahl der monatlich zuleistenden Arbeitszeit |
| start_date | DateTimeField() | Beginn der Gültigkeit des Vertrags |
| end_date | DateTimeField() | Ende der Gültigkeit des Vertrags |
| created_at | DateTimeField(auto_now_add=True) |    |
| created_by | ForeignKey(to=User) |    |
| modified_at | DateTimeField(auto_now=True) |    |
| modified_by | ForeignKey(to=User) |    |
|---------|-----------|--------|