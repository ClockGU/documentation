---
description: Was geschieht mit meinen Daten?
---

# Datenschutz

Clock ist eine Web-App für individuelle Benutzer\*innen.

Das bedeutet, dass man Clock nur mit einem Benutzerkonto und einem Passwort benutzen kann, weil Deine gesammelten Arbeitszeiten nur _Dich_ etwas angehen.

Das bedeutet aber auch, dass die von Dir eingegebenen Daten gespeichert werden. Welche das sind und was damit geschieht, erklären wir in diesem Artikel.

## Gepeicherte Daten

Alle Daten, die Dich als Benutzer\*in betreffen bzw. von Dir eingegeben wurden, werden in einer _Datenbank_ gespeichert. Dazu gehören

* die Daten Deines Benutzerkontos:
  * Login-Name und Passwort\*
  * Email-Adresse
  * Vor- und Nachname
  * Personalnummer \(die bekommst Du von der Uni\)
  * Erstellungsdatum
  * Datum der letzten Änderung
* die Daten für jeden Vertrag, den Du in Clock angelegt hast
  * Vertragsname
  * Start- und Enddatum
  * Stundenzahl
  * Erstellungsdaten \(Datum und Benutzer\)
  * Änderungsdaten \(Datum und Nutzer der letzten Änderung\)
* die Arbeitszeiten, die Du in Clock eingegeben hast
  * Schichtdaten \(Datum & Zeit von Anfang und Ende der Schicht\)
  * zugehöriger Vertrag
  * Schichttyp \(normal, Urlaub, krank\)
  * Notizen und _Tags_
  * Erstellungs- und Änderungsdaten
  * Status der Schicht \(geplante Schicht / bereits exportiert\)
* die "Reports" - monatliche Zusammenfassungen Deiner Arbeitszeit
  * Datum \(Monat und Jahr\)
  * aktuell gearbeitete Stunden
  * zugehöriger Vertrag
  * Erstellungs- und Änderungsdaten

Aus diesen Daten werden die _Stundenzettel_ generiert und zum Download angeboten. Die PDF-Dateien werden nicht gespeichert, sondern bei jedem Export neu erzeugt.

Alle diese Datenstrukturen sind in der [Datenbank-Referenz](../datenbank-referenz/introduction.md) dokumentiert.

_\*\) wir sind gerade dabei, mit dem HRZ die Authentifizierung über LDAP zu ermöglichen. Damit wird es möglich sein, Dich mit Deinem HRZ-Login und Passwort anzumelden. Das Passwort wird dann nicht bei uns gespeichert, sondern von einem Server beim HRZ geprüft._

## Welche anderen Daten werden noch gespeichert?

Beim Zugriff auf den Dienst über das Internet werden sowohl von Deinem Provider als auch von unserem Server routinemäßig Zugriffsdaten gespeichert \(IP-Adresse und Zugriffszeit\). Diese werden aber nicht in der Clock-Datenbank gespeichert.

Wenn ein Fehler auftritt oder Du das Feedback-Formular nutzt, um uns eine Nachricht zu schicken, werden einige Deiner Daten vom Fehlerüberwachungsdienst _Sentry_ erfasst, der auf unserem Server läuft. Dies ermöglicht uns, genauer zu verstehen, warum ein Fehler auftritt.

## Wo liegen meine Daten?

Die Clock-Datenbank liegt auf einem Server der studentischen Gruppe von _Physik Online_ und steht im Institut für Theoretische Physik am Campus Riedberg. Demnächst soll Clock auf einen Server des Hochschulrechenzentrums \(HRZ\) umziehen.

Die Übermittlung zwischen Deinem Gerät und Clock erfolgt verschlüsselt über eine SSL-Verschlüsselung.

## Wer kann meine Daten einsehen?

Eigentlich nur Du. "Eigentlich" deshalb, weil die Administratoren, die Clock betreuen \(und weiterentwickeln!\), aus technischen Gründen Zugriff auf die Datenbank haben müssen.

Es ist möglich, alle Daten in der Datenbank zu anonymisieren, so dass man nicht einfach Informationen im Klartext anschauen kann. Wir prüfen derzeit die Einrichtung einer solchen Anonymisierung - Allerdings erschwert das auch die Möglichkeit, individuellen Support zu leisten.

Die Administratoren kontrollieren zwar auch die Verschlüsselung und können die gespeicherten Daten - _theoretisch_ - wieder entschlüsseln. Aber das werden sie nicht tun, ohne Dich zu fragen oder ohne von Dir dazu aufgefordert zu werden.

## Kann ich meine Daten einsehen?

Prinzipiell enthält Clock nur Daten, die Du selbst eingegeben hast - entweder durch das manuelle Eintragen oder durch das live-Clocken von Schichten. Diese kannst Du immer einsehen.

Auch die in Deinem User-Account hinterlegten Daten kannst Du einsehen \(auch die, die Du nicht ändern kannst\).

## Kann ich meine Daten löschen?

Einzelne Schichten kannst Du jederzeit selbsttätig löschen, sofern sie noch nicht exportiert sind.

Du kannst alle Daten komplett löschen indem Du Deinen Useraccount löschst bzw. zurücksetzt \("Recht auf Vergessenwerden"\).

{% hint style="info" %}
Aus technischen Gründen bleiben die Daten in \(verschlüsselten\) Sicherheitskopien erhalten. Bei der Wiederherstellung des Systems nach einem Datenverlust werden Deine gelöschten Daten nicht wiederhergestellt.
{% endhint %}

## Darf ich meine Daten haben?

Gemäß den Anforderungen der [DSGVO](https://dsgvo-gesetz.de) \(Artikel 15 & 20\) wird es eine Möglichkeit geben, alle Deine Daten in einer gängigen maschinenlesbaren Form zu exportieren.

## Kann ich Euch das alles glauben?

Clock ist ein Projekt von Studis für Studis - das haben wir bei den Vereinbarungen mit den offiziellen Stellen der Uni \(PersonalServices\) auch immer wieder klar gemacht.

Außerdem ist Clock _Open Source_: Alle funktionalen Programmteile und Informationen sind öffentlich und können von Menschen mit entsprechenden Programmierkenntnissen nachvollzogen werden.

Aber natürlich geht es hier um Vertrauen. Du bist jederzeit eingeladen, mit uns direkt ins Gespräch zu kommen: clock-kontakt@dlist.uni-frankfurt.de

