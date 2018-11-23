---
description: User Stories bezogen auf die Shift Models
---

# Shift Model

Da das Shift Model die tatsächlich gearbeitet Zeit eines Nutzers darstellt ist heir eine größere Anzahl an Interaktionen
zu erwarten welche im folgenden aufgelistet sind:

Der Nutzer sollte in der Lage sein ...

* eine Schicht für den momentanen Monat zu erstellen. (manuelles Erstellen)
* eine Schicht im momentanen Monat zu bearbeiten.
* eine Schicht im momentanen Monat zu löschen.
* eine Schicht einzustechen.
* eine Schicht auszustechen.
* eine Schicht von einem anderen Endgerät auszustechen.
* einer Schicht einen `type` zuzuordnen.
* zukünftige, wiederkehrende Schichten einzuplanen.
* zukünftig geplante Schichten zu löschen.
* zukünftig geplante Schichten, nach deren verstreichen, zu bestätigen/überarbeiten.
* eine Schicht einem Vertrag zuzuweisen.
* eine Schicht von einem Vertrag zu entfernen.
* `tags` zu einer Schicht hinzuzufügen.
* `tags` von einer Schicht entfernen.
* `notes` zu einer Schicht hinzuzufügen.
* `notes` von einer Schicht entfernen.


Anmerkungen:

Die Userführung für das Stechen/Erstellen einer Schicht ist so geplant: 
Der Nutzer wählt über eine Ansicht aller seiner Verträge einen Vertrag aus, für den er im Folgenden plant zu arbeiten.
Anschließend wird ihm die Möglichkeit gegeben eine Schicht manuell nachzutragen / zu planen oder einzustechen. Möchte
der Nutzer eine Schicht von einem Vertrag entfernen wird ihm angeboten die Schicht zu löschen oder er gelangt zurück zur
Ansicht aller Verträge und wählt einen neuen Vertrag aus.

Die Userführung für das bestätigen/überarbeiten einer verstrichenen "geplanten Schicht" ist
wiefolgt geplant:
Der Nutzer sieht nach dem Login ein Pop-Up mit allen, seit denm letzten Login, verstrichenen
geplanten Schichten (lediglich Kerndaten der Schichten werden angezeigt). Hier soll der User
nun die Möglichkeit haben via Checkboxen einzelne Schichten oder, über eine seperate Checkbox,
alle Schichten zu bestätigen. Nicht ausgewählte Schichten werden im Anschluss im
"Bearbeitungsmodus" angezeigt, sodass der Nutzer diese nach Belieben abändern und abspeichern/bestätigen
bzw. löschen kann.

