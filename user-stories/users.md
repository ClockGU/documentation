---
description: User Stories im Bezug auf die User Models
---

# User Model

Da das *User-Model* direkt den Account eines Nutzers darstellt, sind die erwarteten Aktionen limitiert und werden im Folgenden aufgelistet:

Ein Nutzer sollte in der Lage sein ...

* ... sein User-Objekt zu erstellen (Create User = Registrierung).
* ... sein User-Objekt zu löschen (Delete User).
* ... den `first_name` und `last_name` zu aktualisieren.
* ... seine `email` zu aktualisieren.
* ... das `password` zu aktualisieren.

#### Bemerkung:

Das Löschen des Accounts (vgl. Art. 17 DSGVO) ist ein kritischer Punkt: Formal gilt der Account nach dieser Aktion als gelöscht und ein Nutzer kann sich nicht mehr anmelden. Praktisch ist der Account allerdings nur _inaktiv_, da die Daten eines ehemaligen Beschäftigten für eine gewisse Zeit aufbewahrt werden müssen (§17 MiLoG).
