---
description: Definition des ClockedInShift Models
---

# ClockedInShift Model

Das _ClockedInShift Model_ dient zur Speicherung einer eingestochenen aber nicht beendeten Schicht. Sie repräsentiert den persistenten Zustand, in dem ein Nutzer im Frontend auf einem Gerät eingestochen hat, dort die Schicht allerdings nicht beendet hat. Durch das zwischenspeichern ist es nun möglich, von einem anderen Gerät, einer anderen Browsersitzung oder nachträglich \(zu einem anderen Zeitpunkt\) auszustechen. Das Model ist wie folgt definiert:

| Feldname | Feld Type | Nutzung |
| :--- | :--- | :--- |
| id | UUIDField\(primary\_key= True, , default=uuid.uuid4, editable=False, unique=True\) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation einer Schicht in der Datenbank benutzt |
| user | OneToOneField\(to=User, on\_delete=models.CASCADE\) | Einzigartige Relation zu einem Usereintrag |
| contract | OneToOneField\(to=Contract, on\_delete=models.CASCADE\) | Relation zu einem Vertragseintrag |
| started | DateTimeField\(\) | Startzeit und Datum |
| created\_at | DateTimeField\(auto\_now\_add=True\) | Timestamp \(Zeitpunkt\), wann der Eintrag erstellt wurde |
| created\_by | ForeignKey\(to=User\) | User, von dem der Eintrag erstellt wurde |
| modified\_at | DateTimeField\(auto\_now=True\) | Timestamp, an dem der Eintrag zuletzt modifiziert wurde |
| modified\_by | ForeignKey\(to=User\) | User, der den Eintrag zuletzt modifiziert hat |

## Bemerkung

Die Einschränkung, dass für jeden Nutzer nur ein Eintrag in der _ClockedInShift_-Tabelle existieren darf ist durch das `OneToOneField(to=User)` realisiert.

