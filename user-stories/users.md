---
description: User Stories bzgl. des User Models
---

# User Model

Da das User Model direkt den Account eines Nutzers darstellt sind die erwarteten Aktionen sehr limitiert und werden 
im Folgenden aufgelistet :

Ein Nutzer sollte in der Lage sein ...

* sein User Objekt zu erstellen. (Create User - Registrierung)
* sein User Objekt zu löschen.   (Delete User)
* den `first_name` und `last_name` zu updaten.
* die email zu updaten.
* das `password` zu updaten.

Hierbei ist ein kritischer Punkt das Löschen des Accounts. Formal gilt der Account als gelöscht nach dieser Aktion und 
ein Nutzer kann sich nicht mehr mit den Logindaten einloggen. Praktisch ist er allerdings nur _inaktiv_ da auch die
Daten eines ehemaligen Beschäftigten aufbewahrt werden müssen.

