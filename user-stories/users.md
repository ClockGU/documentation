---
description: User Stories im Bezug auf die User Models
---

# User Model

Da das User Model direkt den Account eines Nutzers darstellt, sind die erwarteten Aktionen limitiert und werden 
im Folgenden aufgelistet:

Ein Nutzer sollte in der Lage sein ...

* sein User Objekt zu erstellen. (Create User - Registrierung)
* sein User Objekt zu löschen.   (Delete User)
* den `first_name` und `last_name` zu aktualisieren.
* die E-Mail zu aktualisieren.
* das `password` zu aktualisieren.

Hierbei ist ein kritischer Punkt das Löschen des Accounts. Formal gilt der Account nach dieser Aktion als gelöscht und 
ein Nutzer kann sich nicht mehr anmelden. Praktisch ist der Account allerdings nur _inaktiv_, da die
Daten eines ehemaligen Beschäftigten aufbewahrt werden müssen.

