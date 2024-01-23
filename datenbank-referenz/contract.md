---
description: Definition des Contract Models
---

# Contract Model

Das _Contract-Model_ stellt einen Vertrag eines Users dar. Ein User kann gemäß der Vorgaben mehrere Verträge haben, für die jeweils unterschiedlich viele Stunden Arbeitszeit zu leisten sind. Das Model ist wie folgt definiert:

| Feldname             | Feld Type                                                                        | Nutzung                                                                                                                               |
|:---------------------|:---------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| id                   | UUIDField\(primary\_key= True, default=uuid.uuid4, editable=False, unique=True\) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation eines Users in der Datenbank benutzt |
| user                 | ForeignKey\(to=User\)                                                            | Relation zu einem Usereintrag                                                                                                         |
| name                 | CharField\(\)                                                                    | Vom User vergebener Name des Vertrags                                                                                                 |
| minutes              | PositiveIntegerField\(\)                                                         | Anzahl der monatlich zu leistenden Arbeitszeit in Minuten                                                                             |
| start\_date          | DateField\(\)                                                                    | Vertragsbeginn                                                                                                                        |
| end\_date            | DateField\(\)                                                                    | Vertragsende                                                                                                                          |
| initial_carryover_minutes     | IntegerField()                                                                   | Übertrag aus dem AZK für den Startmonat                                                                                               |
| initial_vacation_carryover_minutes | IntegerField()                                                                   | Urlaubsübertrag aus dem AZK für den Startmonat                                                                                        |                                                                            
| worktime_model_name  | CharField()                                                                      | Arbeitszeitmodel Auswahl aus `VALIDATOR_CLASS_NAMES`                                                                                  |                                                                                 |
| percent_fte          | FloatField()                                                                     | Prozent der Vollzeit-Äquivalenten Stelle                                                                                              |
| created\_at          | DateTimeField\(auto\_now\_add=True\)                                             | Timestamp \(Zeitpunkt\), an dem der Eintrag erstellt wurde                                                                            |
| created\_by          | ForeignKey\(to=User\)                                                            | User, der den Eintrag erstellt hat                                                                                                    |
| modified\_at         | DateTimeField\(auto\_now=True\)                                                  | Timestamp, an dem der Eintrag zuletzt verändert wurde                                                                                 |
| modified\_by         | ForeignKey\(to=User\)                                                            | User, der den Eintrag zuletzt modifiziert hat                                                                                         |
| ---------            | -----------                                                                      | --------                                                                                                                              |

## Bemerkung

Die Felder `start_carry_over` und `month_start_clocking` dienen der akuraten Abbildung des Falls,
dass ein Nutzer nicht zu Beginn seines Arbeitsverhältnisses beginnt Clock zu nutzen sondern einige Monate
später. Zu diesem Zeitpunkt existiert für den User womöglich bereits ein Übertrag aus dem Vormonat und er
möchte für die vergangenen Monate keine Schichten eintragen. Mit diesen beiden Feldern ist es uns möglich
Report's erst ab `month_start_clocking` mit einem `start_carry_over` als default "carry_over" zu erstellen.
