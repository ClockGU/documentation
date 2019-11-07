---
description: User Stories bezogen auf das ClockedInShift Model
---

# ClockedInShift

Da das _Shift_ Model nur zum zwischenspeichern einer "Clocked-In", also live eingestochenen und noch fortlaufenden Schicht,
dient sind hier folgende Aktionen zu erwarten:

Der Nutzer sollte in der Lage sein

* ... eine Schicht einzustechen.
* ... eine eingestochene Schicht zu einem späteren Zeitpunkt auszustechen.

## Anmerkung:

Wichtiger Unterschied zwischen "einstechen" und "erstellen": Mit "einstechen" ist gemeint,
dass der Nutzer nicht wissentlich ein Objekt erstellt sondern dieses automatisch von dem Frontend erstellt wird.

Erklärung zu "ausstechen": Das "Ausstechen geschieht lediglich im Frontend.
Dabei wird das Objekt angefragt, die Daten mit Endzeit etc. als _Shift_ gespeichert und anschließend
das _ClockedInShift_ Objekt gelöscht.

Erklärung "späterer Zeitpunkt": Hierbei wird darauf abgezielt, dass die Internetverbindung
eines Nutzers abbrechen könnte, die Website ausversehen geschlossen wird oder der Nutzer das Endgerät
wechelt (Smartphone <--> Tablet <--> Labtop etc.).