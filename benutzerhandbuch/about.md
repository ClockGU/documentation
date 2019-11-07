---
description: Das CLOCK Projekt aus technischer Perspektive
---

# Zur Technik

Clock ist eine _Web-App,_ die aus verschiedenen Komponenten besteht:

### Backend

Das, was die Benutzer\*innen nicht zu sehen bekommen. Dazu gehören:

* die Datenbank \(in der alle Daten gespeichert werden\)
* die Schnittstelle \(über die man Daten auslesen und speichern kann\) 

Die Clock-Datenbank basiert auf [PostGreSQL 9.4+](https://www.postgresql.org/). Die Schnittstelle ist mit dem [Django-REST](https://www.django-rest-framework.org/)-Framework umgesetzt. Eine solche Schnittstelle wird auch als _API_ \(Advanced Programming Interface\) bezeichnet.

### Frontend

Das, was Du als Benutzer\*in zu sehen bekommst: die Benutzeroberfläche \(oder auch das _User-Interface_ oder auch _UI_\). Das Frontend kommuniziert über die _API_ mit der Datenbank .

Das Frontend ist mit dem Javascript-Framework [Vue.js](http://vuejs.org) umgesetzt, mit dem man Web-Apps programmieren kann, die in jedem \(modernen\) Webbrowser laufen.

### Design

Apps verwenden wir \(fast\) alle - auf mobilen oder nichtmobilen Geräten - und da gibt es viele Varianten, die Benutzeroberfläche zu gestalten.

Wir halten uns an die Designsprache [Material Design](http://material.io), die von Google entwickelt wurde und zu einem gewissen Standard im Web und insbesondere auf Android-Geräten geworden ist.

Diese Richtlinien beschreiben die Darstellung einzelner Komponenten, aber auch die Positionierung von Menüs, Buttons etc. Dabei wird auf Logik, Konsistenz und Klarheit geachtet.

Zur Umsetzung von Material Design in Vue.js kommt die Design-Bibliothek [Vuetify](http://vuetifyjs.com) zum Einsatz.

## History

Die Idee von Clock gibt es schon seit etwa 2014. Damals wurden die monatlichen Stundenzettel neu eingeführt und das war ziemlich anstrengend und umständlich, denn alles musste von Hand eingetragen werden.

#### Beginnings

Ein HiWi \(und sein Chef\) hatten die Idee, dafür ein Programm zu verwenden, mit dem man wie mit einer Stechuhr ein- und ausstechen konnte. Natürlich wurde zuerst recherchiert, ob man nicht einfach vorhandene Tools verwenden konnte. Diese waren aber entweder teuer oder so komplex, dass sie für einen simplen Stundenzettel einfach zu umständlich gewesen wären.

Also ergab sich daraus das Vorhaben, eine Web-Anwendung zu bauen, die genau das kann, was sie soll - und nicht mehr. Außerdem war das ein tolles Projekt, um zu lernen, wie man eine solche Anwendung plant und programmiert.

#### Clock 1.0

Die erste Version von Clock sah vielversprechend aus, hatte aber noch einige Fehler und war daher immer ganz knapp vor dem Punkt, an dem man das Produkt hätte richtig veröffentlichen können.

Als dann Arbeitszeitkonto \(AZK\) nach MiLoG eingeführt wurden, war klar, dass ein Umbau des alten Codes umständlicher werden würde als ein vollständiger Neubau.

Außerdem hatten sich Programmierkenntnisse weiterentwickelt und es gab neue, etablierte Technologien, die für den Zweck besser geeignet waren.

Vor allem aber gab es eine Personalabteilung, die sehr interessiert daran war, eine gute Alternative zu der nicht ganz perfekten Excel-Methode anbieten zu können und sich vorstellen konnte, HiWi-Mittel zu investieren.

#### Der Weg zu Clock 2.0

Da man aus den Fehlern der Vergangenheit lernen soll, wurde das neue Projekt viel sorgfältiger geplant und ganz neu aufgezogen.

In einem ersten Schritt \(mit nicht wenigen Mails und Meetings\) wurden [_User Stories_](../user-stories/introduction.md) geschrieben. Diese beschreiben, was die Anwendung aus Sicht eines Users können soll.

Die äußeren Anforderungen an die App \(z.B. die Regeln des Arbeitszeitkontos, Pausenzeiten etc.\) wurden außerdem als [_Business Rules_](../business-rules/introduction.md) formuliert.

Daraus ergeben sich sehr klare Anforderungen an die Anwendung und an die benötigten [Datenmodelle](https://github.com/ClockGU/documentation/tree/c22fe7cad3af1ba515417bf5663bb73f6193bda9/database/introduction.md).

### Test... Test...

Ein neues Produkt muss auch geprüft werden: ob es tut, was es soll, ob es keine Fehler produziert und überhaupt benutzbar ist. Deshalb wird zuerst für einige Wochen ein "Alpha-Test" mit ausgewählten Benutzer\*innen durchgeführt, um ein erstes Gefühl von Außenstehenden zu bekommen. Danach wird die App für alle HiWis in einem offenen "Beta-Test" freigegeben.

Während dieser Beta-Phase werden noch viele Details nachgearbeitet, wir arbeiten aber schon mit echten Daten und man kann echte Stundenzettel erzeugen \(und wahrscheinlich wird man gar nicht merken, wenn das "Beta" wegfällt\).

Dennoch ist Feedback an die Entwickler sehr wichtig - ob es um Fehler oder Verbesserungsvorschläge geht. Wie man diese Rückmeldung gibt, steht genauer im Kapitel [Feedback](how2feedback.md).

## Mitarbeit

Wenn Du Dich mit der Technik in Frontend und Backend auskennst und mit uns fachsimpeln oder etwas zum Projekt beitragen möchtest, dann kannst Du Dich gerne mit uns in Verbindung setzen: [clock-kontakt@dlist.uni-frankfurt.de](mailto:clock-kontakt@dlist.uni-frankfurt.de)

