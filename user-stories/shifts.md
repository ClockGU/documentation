---
description: User Stories bezogen auf die Shift Models
---

# Shift

Da das _Shift-Model_ die tatsächlich gearbeitete Zeit eines Nutzers darstellt, ist heir eine größere Anzahl an Interaktionen zu erwarten, welche im Folgenden aufgelistet sind:

Der Nutzer sollte in der Lage sein ...

* ... eine Schicht zu erstellen \(manuelles Erstellen\).
* ... eine Schicht im laufenden Monat zu bearbeiten.
* ... eine Schicht im laufenden Monat zu löschen.
* ... eine Schicht live ein- und auszustechen \(in einer Sitzung\).
* ... einer Schicht einen `type` zuzuordnen \(Schicht/Krank/Urlaub\).
* ... zukünftige, wiederkehrende Schichten einzuplanen.
* ... zukünftig geplante Schichten zu löschen.
* ... zukünftig geplante Schichten nach deren verstreichen zu bestätigen/überarbeiten.
* ... eine Schicht einem Vertrag zuzuweisen.
* ... eine Schicht von einem Vertrag zu entfernen.
* ... `tags` zu einer Schicht hinzuzufügen.
* ... `tags` von einer Schicht zu entfernen.
* ... `notes` zu einer Schicht hinzuzufügen.
* ... `notes` von einer Schicht zu entfernen.

## Anmerkungen:

Die Benutzerführung für das Stechen/Erstellen einer Schicht ist so geplant:

Der Nutzer wählt über eine Ansicht aller seiner Verträge einen Vertrag aus, für den er im Folgenden plant, zu arbeiten. Anschließend wird ihm die Möglichkeit gegeben, eine Schicht manuell nachzutragen / zu planen oder einzustechen. Möchte der Nutzer eine Schicht von einem Vertrag entfernen, wird ihm angeboten, die Schicht zu löschen oder er gelangt zurück zur Ansicht aller Verträge und wählt einen neuen Vertrag aus.

Die Benutzerführung für das Bestätigen/Überarbeiten einer verstrichenen "geplanten Schicht" ist so geplant:

Dem Nutzer wird nach dem Login ein Pop-Up mit allen seit dem letzten Login verstrichenen geplanten Schichten angezeigt \(lediglich Kerndaten der Schichten\). Hier soll der Nutzer nun die Möglichkeit haben, einzelne Schichten über Checkboxen zu bestätigen \(sowie alle Schichten gesammelt über eine eigen Checkbox\). Nicht ausgewählte Schichten werden im Anschluss im "Bearbeitungsmodus" angezeigt, sodass der Nutzer diese nach Belieben abändern und abspeichern/bestätigen bzw. löschen kann.

