---
description: Definition des User Models
---

# User

Das User Model dient zur Repräsentation der Kerndaten eines Users, welche zur Identifikation und Nutzung des
Services nötig sind. Bei der folgenden Definition entsprechen der Feldname dem Namen des Feldes im Code, der Feldtyp
der Feldklasse im Code und die Nutzung der angedachten Verwenudng des Feldes (falls nicht eindeutig ersichtlich) :

|Feldname | Feld Type | Nutzung|
|---------|-----------|--------|
| id      | UUIDField(primary_key= True) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation eines Users in der Datenbank benutzt|
| email   | EmailField() |     |
| first_name | CharField() |   |
| last_name | CharField()  |   |
| personal_number | CHarField() | Die Personalnummer wird für den Stundenzettel benötig und änder sich **nie** |
| created_at| DateTimeField(auto_now_add=True)| Timestamp wann der Usereintrag erstellt wurde   |
| modified_at| DateTimeField(auto_now=True)| Timestamp wann der Usereintrag zu letzt geändert wurde |
|---------|-----------|--------|


Diese Tabelle stellt nun alle Daten dar welche ein Nutzer dem Service zurverfügung stellt bzw. die über den Nutzer 
beim erstmaligen Registrieren gespeichert werden. Hierbei ist es wichtig anzumerken dass auf das benutzen simpler Id's 
verzichtet wird um spätere API abfragen von Nutzerdaten zu anonymisieren.
