---
description: Business Rules für das Shift Model
---

# Shift Model

Für das *Shift*-Model gelten die im Folgenden aufgelisteten Einschränkungen:

Einem Nutzer ist es nicht möglich ...

* ...auf Schichten zuzugreifen, die *nicht* ihm gehören.
* ...Schichten zu bearbeiten, die *nicht* ihm gehören.
* ...Schichten zu löschen, die *nicht* ihm gehören.
* ...Schichten zu bearbeiten, die *bereits* exportiert wurden.
* ...Schichten zu lösche,n die *bereits* exportiert wurden.
* ...eine Schicht in der Zukunft zu erstellen, welche *nicht* als geplant gilt.
* ...eine Schicht in der Zukunft einzustechen.
* ...eine Schicht in der Zukunft auszustechen.
* ...eine Schicht zu erstellen, deren Ende *vor* deren Anfang ist (`duration > 0`).
* ...eine Schicht zu erstellen, deren Vertrag erst in der Zukunft beginnt.

Ferner gelten folgende Einschränkungen:

* eine Schicht mit `was_reviewed=False` wird bei der Berechnung des Reports *nicht* beachtet.


#### Anmerkung:
Der Begriff "Zukunft" bezieht sich auf die Zeit nach dem versuchten Durchführen der Aktion.
Bsp.: Jetzt ist der 01.01.2020 13:47:31. Als Zukunft gilt jede Zeit, die eine Differnez größer Null zu dieser `DateTime`
besitzt.
