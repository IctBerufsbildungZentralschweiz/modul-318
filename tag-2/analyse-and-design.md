# 📖 Analyse & Design

## 💬 Klassendiskussion

* Was versteht ihr unter Analyse & Design?
* Wer hat schon an Kundensoftware gearbeitet?



## Einleitung

Analyse: WAS muss das System können?  
Design: WIE soll das System gebaut werden?



Wie wir bereits gestern besprochen haben, ist eines der essentiellen Aufgaben, zu verstehen, was der Kunde oder die Kundin wirklich möchte.

![Verst&#xE4;ndnis von Anforderungen](../.gitbook/assets/image%20%28104%29.png)

Kommunikation ist alles! Wenn der Kunde von Anfang an miteinbezogen wird und durch eine [agile Vorgehensweise](../tag-1/klassische-vs.-agile-vorgehensweise.md#agile-vorgehensweise-z-b-scrum) auch in jedem Schritt beteiligt ist, sind Missverständnisse viel unwahrscheinlicher oder können schon sehr früh aus dem Weg geräumt werden.

In der Anforderungsanalyse findet aber bereits sehr viel Kommunikation statt. Es gibt Diskussionen, grobe Besprechungen in Workshops, Interviews oder sogar Beobachtung von Endbenutzern am Arbeitsplatz. Das alles muss auch dokumentiert sein.

Nun geht es darum, Anforderungen von Kunden zu analysieren und in Formen zu bringen bzw. so Abzubilden, wie sie uns für die Umsetzung möglichst nützlich sind. Dafür gibt es zahlreiche Tools und Methoden.



## Use Case Diagramm

Eine Möglichkeit, um sehr schnell und abstrakt einen Überblick über die Anforderungen zu erhalten, ist das UML Use Case Diagramm.

![](../.gitbook/assets/image%20%2896%29.png)

Dieses Use Case Diagramm zeigt die Use Cases eines Online Shops, der zwei verschiedene Anwendertypen hat. Ein Verkäufer, der Artikel erfasst und Bestellungen verarbeitet und einen Kunden, welcher Artikel auswählt und bestellt.

Ein Use Case Diagramm stellt keine Logik dar, z.B. dass der Kunde zuerst Artikel auswählen muss, bevor er eine Bestellung abschicken kann. Darum geht es aber auch nicht im Use Case Diagramm. Es geht nur darum, schnell einen Überblick über die Funktionen einer Software zu erhalten.



## User Story

> "User Stories beschreiben die Anforderungen an ein Produkt oder Service aus Sicht des Nutzers. Als Format ist die User Story ein zentrales Werkzeug in der Zusammenarbeit agiler Teams. Ihr Einsatzgebiet reicht von der Validierung von Kundenbedürfnissen bis zur Anforderungsformulierung in Scrum Teams." - Andreas Diehl

User Stories sind einerseits dazu da, die Kundenbedürfnisse / Anforderungen abzubilden, dienen zugleich aber auch als Arbeitspakete für die Entwickler, und können durch Aufwandschätzung auch als Basis einer Offerte dienen. Das macht sie sehr wertvoll.

_Nachfolgende Texte sind \(z.T, leicht angepasste\) Ausschnitte aus dem Artikel:_ [_User Stories – Universelle Sprache in agilen Teams_](https://digitaleneuordnung.de/blog/user-stories/)\_\_

### User Story Definition

User Stories \(dt. Nutzer- oder Anwendererzählung\) haben ihren Ursprung in der agilen Softwareentwicklung. Im Gegensatz zu einer klassischen Spezifikation beschreibt die User Story ausschließlich die Erwartungen des Nutzers an die Funktionalität einer Software und nicht etwa WIE die Anforderung umzusetzen ist.

Heute sind User Stories auch über die Softwareentwicklung hinaus eines der zentralen Werkzeuge, um Anforderungen zu formulieren und  zu diskutieren. Dabei bilden mehrere User Stories gemeinsam einen Use Case.

Der User Case ist wiederum, was wir im Use Case Diagramm modellierten.

### Struktur einer User Story

Die Beschreibung einer User Story ist wie folgt aufgebaut:

> `Als <Nutzer> möchte ich <Funktion>, um <Wert>`

Das heißt, eine User Story beantwortet die Fragen WER möchte WAS und WARUM. Lass uns auf die drei Bestandteile im Einzelnen schauen.

#### &lt;Nutzer&gt; – Wer?

Den Platzhalter &lt;Nutzer&gt; füllst Du mit Rollen bzw. deinen Personas. Eine [Persona ist ein typischer Vertreter deiner Zielgruppe](https://digitaleneuordnung.de/blog/personas-erstellen/). Die Rolle des Nutzers kann auch durch den jeweiligen Kontext definiert sein. So kann die gleiche Rolle z.B. für unterschiedliche Personas gelten und das Verhältnis zu deinem Produkt beschreiben.

{% hint style="info" %}
**Beispiel**: Du bist aktuell in der Rolle "Teilnehmer des Kurses". Das sagt mir zwar, dass du das EFZ in Informatik machst, sagt aber noch nichts darüber, ob du eine Lehre als Informatiker in Systemtechnik oder Applikationsentwicklung machst, oder welche Rolle du in deiner Firma wahrnimmst.
{% endhint %}

Wie detailliert Du den Platzhalter &lt;Nutzer&gt; füllst, ist von der User Story selbst, aber auch von der Reife deines Vorhabens abhängig. Für den passenden Detaillierungsgrad gibt es kein richtig oder falsch. Das Wichtigste ist, dass für Dich und dein Team mit dem gewählten &lt;Nutzer&gt; eine für Dich aussagekräftige User Story entsteht.

#### &lt;Funktion&gt; – Was?

Den Platzhalter &lt;Funktion&gt; ersetzt Du mit der Erwartung, den Zielen und Wünschen des &lt;Nutzers&gt;. Damit beantwortest Du die Frage, WAS der Kunde braucht und erwartet. Wenn du bereits ein Produkt am Markt anbietest, erhältst Du sicher viele gewünschte Funktionen direkt vom Nutzer. In früheren Phasen deines Projektes kannst Du basierend auf deiner Erfahrung Annahmen formulieren, welche &lt;Funktion&gt; der &lt;Nutzer&gt; erwartet.

{% hint style="info" %}
**Beispiel**: Auch wenn Du und ich nicht direkt darüber gesprochen haben, habe ich durch meine tägliche Arbeit als Softwareentwickler und Berater ein gutes Verständnis, welche Fragen du im Zusammenhang mit der Erstellung einer User Story mitbringst. Die &lt;Funktion&gt; dieser Lektion ist "User Stories verstehen". Das heisst, daraus resultiert folgende User Story:

> Als _Teilnehmer dieses Kurses_ möchtest Du **User Stories verstehen**, ….
{% endhint %}

#### &lt;Wert&gt; – Warum?

Der Platzhalter &lt;Wert&gt; beantwortet die Frage nach dem WARUM. Auch wenn der Satzbau dazu verleitet diesen Nebensatz weg zu lassen, ist eine User Story ohne diesen Zusatz nicht komplett.

Das heißt, erst mit dem &lt;Wert&gt; bringst Du zum Ausdruck, warum die Erreichung der &lt;Funktion&gt; für den &lt;Nutzer&gt; überhaupt wichtig ist und welchen Mehrwert die Erfüllung der User Story schafft. Spätestens an dieser Stelle bietet Dir die User Story eine ehrliche Reflektion, wie gut Du Dich bereits mit den Anforderungen deiner Kunden auseinander gesetzt hast. Anforderungen aufzunehmen ist einfach \(z.B. weil der Kunde nach einer Funktion schreit\). Zu verstehen warum es für ihn wichtig ist, gibt Dir und deinem Team aber erst den notwendigen Kontext.

{% hint style="info" %}
**Beispiel**: Dein erwarteter Mehrwert aus der aktiven Teilnahme an diesem Kurs kann sein, dass du eine gute Modulnote erhälst, kann aber auch sein, dass du ab morgen User Stories anwenden möchtest. Daher würde die User Story hier so aussehen:

> Als _Teilnehmer dieses Kurses_ möchte ich _User Stories verstehen,_ damit **ich den ÜK mit einer guten Note abschliessen kann**.

oder

> Als _Teilnehmer dieses Kurses_ möchte ich _User Stories verstehen,_ damit ich **ab morgen User Stories verwenden kann**.
{% endhint %}



### Abnahmekriterien

In der Praxis trifft man meist auf User Stories, die nebst der Beschreibung nach dem obigen Schema auch **Abnahmekriterien** \(auch Akzeptanzkriterien oder Acceptance Criteria genannt\) definiert haben. Sie dienen dazu, während eines Sprints die Story als "Abgeschlossen" anzuschauen, nämlich dann, wenn die Punkte unter Abnahmekriterien alle zutreffen.

Beispiel:

{% hint style="info" %}
**Story 5: User Stories verstehen** 

Als Teilnehmer dieses Kurses möchte ich User Stories verstehen, damit ich den ÜK mit einer guten Note abschliessen kann. 

Abnahmekriterien: 

* Der Instruktor hat alle Punkte erklärt 
* Der Kursteilnehmer hat die ganzen Unterlagen zum Thema "Analyse & Design" gelesen
* Der Kursteilnehmer hat die Übung "Projektanforderungen analysieren" abgeschlossen
{% endhint %}

Die Abnahmekriterien können teilweise etwas das "WIE" \(Design\) beschreiben, denn sie werden meist erst kurz vor der Umsetzung verfasst, wenn mehr technische Informationen vorhanden sind. Das ist der Moment, in dem die User Story auch als Arbeitspaket verwendet werden kann.

Wenn ein Entwickler eine Story für sich abgeschlossen hat, wird im Code Review meist auch auf die Abnahmekriterien eingegangen, um zu sehen, ob die Story auch wirklich abgeschlossen ist.



### Granularität

Es ist wichtig, Funktionalität in einer guten Granularität auf User Stories aufzuteilen. Eine User Story pro Funktionalität.

Ist Beispielsweise ein Login in einem System gewünscht, in welchem man auch gleich einen neuen Benutzer hinzufügen kann und das Passwort zurücksetzen kann, wenn man es vergessen hat, macht es keinen Sinn, das alles in eine User Story zu packen.

Hier könnte man Beispielsweise drei User Stories erstellen:

* Story 1: **Login** Als _registrierter Benutzer_ möchte ich _mich im System einloggen_ können, damit ich _das System mit meinen Berechtigungen verwenden kann_.
* Story 2: **Passwort Vergessen** Als _registrierter Benutzer_ möchte ich _mein Passwort zurücksetzen_ können, damit ich _das System weiterhin verwenden kann, wenn ich das Passwort vergessen habe_.
* Story 3: **Benutzer Erstellen** Als _nicht registrierter Benutzer_ möchte ich _ein Benutzerkonto erstellen_, damit ich _mich im System einloggen kann_.

Das macht auch später für die Umsetzung Sinn. Gibt es mehrere Entwickler im Team, könnten diese drei Stories parallel entwickelt werden.



## Aktivitätsdiagramm

Wie auch das Use Case Diagramm, ist das Aktivitätsdiagramm ein UML Diagramm.

![](../.gitbook/assets/image%20%2864%29.png)

Aktivitätsdiagramme sind eine Möglichkeit, um Programmabläufe zu dokumentieren. Diese Diagrammart wird nun kurz vorgestellt:

Die Ausführung einer Aktivität beginnt beim Startknoten und endet beim Endknoten \(Eselsbrücke: wie eine Zielscheibe\). Es sind auch mehrere Endknoten möglich.

Der wichtigste Baustein im Aktivitätsdiagramm ist die Aktion, als Rechteck mit abgerundeten Ecken dargestellt. Aktionen stellen die einzelnen Schritte dar, aus denen eine Aktivität besteht. Man könnte sagen, sie sind die kleinste, nicht mehr zerlegbare Einheit einer Aktivität.

Alle Aktionen zusammengenommen stellen einen schrittweisen Ablauf dar wie etwa den eines Use-Case oder einer Funktion \(oder einer User Story\). Im Rechteck mit den abgerundeten Ecken wird jeweils eine kurze Beschreibung der **Aktion** angegeben. Diese Beschreibung sollte wie bei Use-Cases kurz, knapp und präzise sein.

**Verzweigungen** ermöglichen es je nach Situation als nächsten Schritt verschiedene Aktionen auszuführen. Die Bedingung für die jeweilige Verzweigung kann direkt auf den entsprechenden Pfeil geschrieben werden \(sh. Beispiel im nächsten Slide\).

Eine **Gabelung** synchronisiert zwei oder mehrere separate Pfade \(oder teilt sie\).

_Quelle:_ [_http://www.highscore.de/uml/aktivitaetsdiagramm.html_](http://www.highscore.de/uml/aktivitaetsdiagramm.html)\_\_

### 💬  Beispiel

![](../.gitbook/assets/image%20%2825%29.png)

* Zu was für einem Use Case könnte dieses Aktivitätsdiagramm gehören?
* Wie könnte eine User Story dazu und die dazugehörigen Abnahmekriterien aussehen?

