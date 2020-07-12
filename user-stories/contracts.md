---
description: User Stories bezogen auf die Contract Models
---

# Contract

Da das _Contract-Model_ dem tatsächlich abgeschlossenen Arbeitsvertrag entspricht, ist die User Story überschaubar. Die Aktionen, die ein Nutzer tätigen kann, sind im Folgenden aufgelistet:

Der Nutzer sollte in der Lage sein ...

* ... einen Contract zu erstellen.
* ... ein `start_date` und `end_date` zu einem Contract hinzuzufügen.
* ... `hours` hinzuzufügen.
* ... einen `name` hinzuzufügen.
* ... einen Contract zu aktualisieren.
* ... einen Contract zu löschen.
* ... in einem Contract festzulegen ab welchem Monat er beginnen möchte Zeiten zu dokumentiern.[^1]
* ... in einem Contract festzulegen mit welchem Arbeitsstundenübertrag er beginnt.[^2]



[^1] : Der User bestimmt somit, ab (inklusiv) welchem Monat er in der Lage sein wird Stundenzettel zu exportieren

[^2] : Diese Möglichkeit sorgt dafür, dass ein User die korekten Arbeitsvertragsdaten eintragen kann obwohl er erst einige Monate später beginnt Clock zu nutzen.
Zu diesem Zeitpunkt ist es durchaus möglich, dass ein User bereits einen Übertrag (positiv oder negativ) an Arbeitszeit angesammelt hat.
