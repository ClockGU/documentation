---
description: Definition des User Models
---

# User Model

Das _User-Model_ dient zur Repräsentation der Kerndaten eines Benutzers, welche zur Identifikation und Nutzung des Services nötig sind. Bei der folgenden Definition entsprechen der Feldname dem Namen des Feldes im Code, der Feldtyp der Feldklasse im Code und die Nutzung der angedachten Verwendung des Feldes \(falls nicht eindeutig ersichtlich\):

| Feldname | Feld Type | Nutzung |
| :--- | :--- | :--- |
| id | UUIDField\(primary\_key= True, default=uuid.uuid4, editable=False, unique=True\) | Eine [UUID](https://de.wikipedia.org/wiki/Universally_Unique_Identifier) wird zur Identifikation eines Users in der Datenbank benutzt |
| username | CharField\(\) | Username des Users |
| password | CharField\(\) | Passwort des Users |
| email | EmailField\(unique=True\) | Emailadresse des Users |
| first\_name | CharField\(\) | Vorname |
| last\_name | CharField\(\) | Nachname |
| personal\_number | CharField\(default=""\) | Die Personalnummer wird für den Stundenzettel benötigt und ändert sich **nie** |
| language | CharField\(choices=\("de", "en"\), default="en"\) | Die vom user präfereierte Spracheinstellung |
| created\_at | DateTimeField\(auto\_now\_add=True\) | Timestamp \(Zeitpunkt\), wann der Usereintrag erstellt wurde |
| modified\_at | DateTimeField\(auto\_now=True\) | Timestamp, wann der Usereintrag zuletzt geändert wurde |
| --------- | ----------- | -------- |

Diese Tabelle stellt alle Daten dar, welche ein Nutzer dem Service zur Verfügung stellt bzw. die über den Nutzer beim erstmaligen Registrieren gespeichert werden. Hierbei ist es wichtig anzumerken, dass auf die Verwendung einfacher ID's verzichtet wird, um spätere API-Abfragen von Nutzerdaten zu anonymisieren.

## Bemerkung:

Das User Model erbt vom in Django bereits vorgesehenen _built-in_ Model [AbstractUser](https://github.com/django/django/blob/master/django/contrib/auth/models.py#L289). Der Grund hierfür ist, dass soviel Django-Code wie möglich benutzt werden soll. Dies bedeutet speziell, dass das Authentifizierungssystem \(Identitätsprüfung\), das Admin-Interface \(Oberfläche zur Verwaltung der Datenbank\) und das Permission-Handling \(Berechtigungsmanagement\) von Django verwendet werden können.

Hinweis: Da Clock keinen Usernamen benötigt, sondern der Login über die E-mailadresse abgewickelt wird, ist das Feld `username` \(geerbt von `AbstractUser`\) obsolet. Da aus oben genannten Gründen das Erben von `AbstractUser` gewünscht ist, wird bei der Erstellung eines Users dessen E-mailadresse **ebenfalls** in das Feld `username` gespeichert.

