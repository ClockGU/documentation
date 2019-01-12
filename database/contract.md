---
description: Definition des Contract Models
---

# Contract

Das Contract Model stellt einen Vertrag eines Users dar. Ein User kann gemäß Vorgaben mehrere Verträge haben für die
jeweils unterschiedlich viele Stunden Arbeitszeit zu leisten sind. Das Model ist wie folgt definiert:

|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True, default=uuid.uuid4, editable=False, unique=True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation eines Users in der Datenbank benutzt|
| user    | ForeignKey(to=User) | Relation zu einem Usereintrag |
| name    | CharField()  | Userdefinierter Name des Vertrags |
| hours   | FloatField() | Anzahl der monatlich zuleistenden Arbeitszeit in Minuten|
| start_date | DateField() | Vertragsbeginn |
| end_date | DateField() | Vertragsende |
| created_at | DateTimeField(auto_now_add=True) |  Timestamp an dem der Eintrag erstellt wurde  |
| created_by | ForeignKey(to=User) |  User der den Eintrag erstellt hat  |
| modified_at | DateTimeField(auto_now=True) |  Timestamp an dem der Eintrag zuletzt modifiziert wurde  |
| modified_by | ForeignKey(to=User) |  User der den Eintrag zuletzt modifiziert hat  |
|---------|-----------|--------|