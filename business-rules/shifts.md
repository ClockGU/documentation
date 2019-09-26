---
description: Business Rules für das Shift Model
---

# Shift Model

Für das _Shift-Model_ gelten die im Folgenden aufgelisteten Einschränkungen:

Einem Nutzer ist es nicht möglich ...

* ... auf Schichten zuzugreifen, die _nicht_ ihm gehören.
* ... Schichten zu bearbeiten, die _nicht_ ihm gehören.
* ... Schichten zu löschen, die _nicht_ ihm gehören.
* ... Schichten zu bearbeiten, die _bereits_ exportiert wurden.
* ... Schichten zu löschen, die _bereits_ exportiert wurden.
* ... eine Schicht in der Zukunft zu erstellen, welche _nicht_ als geplant gilt.
* ... eine Schicht in der Zukunft einzustechen.
* ... eine Schicht in der Zukunft auszustechen.
* ... eine Schicht zu erstellen, deren Ende _vor_ deren Anfang ist \(`duration > 0`\).
* ... eine Schicht zu erstellen, welche nicht am gleichen Tag endet an dem sie auch beginnt.
* ... eine Schicht zu erstellen, welche auf einen Contract verweißt der nicht dem USer gehört.
* ... eine Schicht zu erstellen, welche Tags besitzt die keine `strings` sind.

Ferner gelten folgende Einschränkungen:

* eine Schicht mit `was_reviewed=False` wird bei der Berechnung des Reports _nicht_ beachtet.

## Anmerkung:

Der Begriff "Zukunft" bezieht sich auf die Zeit nach dem versuchten Durchführen der Aktion. Beispiel: Jetzt ist der 01.01.2020 13:47:31. Als Zukunft gilt jede Zeit, die eine Differnez größer Null zu dieser `DateTime` besitzt.

