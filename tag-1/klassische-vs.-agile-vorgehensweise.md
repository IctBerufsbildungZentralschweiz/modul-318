---
description: Klassische vs. Agile Vorgehensweise
---

# 📖 Vorgehensweisen

## Warum gehen IT-Projekte schief?

In klassischen Prozessmodellen, wie dem Wasserfallmodell wurde oft zu Beginn eines Projektes ein sogenanntes Pflichtenheft erstellt, wo alle möglichen Anforderungen aufgeschrieben wurden. Dieses musste dann von Auftraggeber und Auftragnehmer unterschrieben werden und galt als Vereinbarung für das Produkt, welches aus dem Projekt entstehen sollte. 

Das Problem: Oft, oder gar fast immer, haben Programmierer und Kunden nicht die gleiche Vorstellung von einer Lösung.

![Verst&#xE4;ndnis von Anforderungen](../.gitbook/assets/image%20%28104%29.png)

Daher kam es oft vor, dass zu Beginn eines Projektes mit dem Kunden dieses Pflichtenheft angeschaut wurde und unterschrieben, und dann nach Monaten der Entwicklung das Programm "fertig" war und dem Kunden übergeben wurde. Darauf folgte dann auch immer die Ernüchterung. "Das habe ich so nicht bestellt".

### Das Kundenverständnis

Eine der schwersten Aufgaben in der Softwareentwicklung ist es, die Bedürfnisse des Kunden zu verstehen. In der Regel sind Kunden technisch nicht versiert und wissen nicht, was technisch möglich ist.

![](../.gitbook/assets/image%20%2829%29.png)

Der Kunde kennt nur, was er hat. Wenn er sagt, "ich möchte ein schnelleres Pferd", muss man zuerst das Bedürfnis verstehen. Das schnellere Pferd ist nämlich nicht wirklich das Bedürfnis, sondern bereits ein Lösungsvorschlag basierend auf den Kenntnissen des Kunden. **Tatsächlich will er schneller von A nach B kommen**.

Wenn man die Wünsche des Kunden zu wörtlich nimmt, kann das die Lösungsfindung wesentlich einschränken.

### Mögliche Fehlerquellen in Projekten

* Unzureichende Kommunikation 
* Zeitdruck / Zeitmanagement 
* Ressourcen-Planung 
* Ziele falsch gesetzt 
* Unpräzise, stetig ändernde Anforderungen 
* Ungenügendes Testen 
* Projektstatus ungenügend verfolgt

{% hint style="info" %}
Keiner dieser Gründe ist technischer Natur!   
Es geht um: Planung, Vorgehensweise, Management, Kommunikation
{% endhint %}



## Klassische Phasenmodelle

Im klassischen Wasserfallmodell haben die Aktivitäten eine klare Reihenfolge.

![Das Wasserfallmodell](../.gitbook/assets/image%20%2856%29.png)

* Analyse: Projektplan, Offerte, Kalkulation, Pflichtenheft 
* Design: Technische Dokumentation, GUI-Styleguide 
* Codierung: Umsetzung der Software
* Test: Testdokumentation \(Testszenarien\), Testumgebung/-einrichtung
* Integration: Benutzerhandbuch , fertiges System

Erst am Ende kommt das Resultat zum Kunden. Es liegt auf der Hand, dass das Resultat meist nicht den Erwartungen des Kunden entsprach \([siehe Grafik oben](klassische-vs.-agile-vorgehensweise.md#warum-gehen-it-projekte-schief)\).

### Anforderungen ändern sich

![](../.gitbook/assets/image%20%2834%29.png)

Die Welt, die Leute und damit auch die Anforderungen ändern sich laufend. In einem klassischen Projektvorgehen hat man aber nicht die Möglichkeit, sich an neue Gegebenheiten, Erkenntnisse oder Wünsche anzupassen.

### Weitere Probleme der klassischen Vorgehensweise

* Fehler werden spät erkannt. \(späte Entdeckung von Anforderungs-, Analyse- und Designfehlern, oft erst während Integrationstest\) 
* Risiken werden lange mitgeschleppt \(«weil jetzt noch nicht codiert/getestet werden darf»\)
* Nachträgliche Anforderungen können nicht berücksichtigt werden.
* Projektfortschritt ist über lange Zeit nicht messbar.



## Agile Vorgehensweise \(z.B. SCRUM\)

Mit einer agilen Vorgehensweise kann man diese Probleme grösstenteils umgehen.

Das Team von Softwareentwicklern arbeitet in kleinen Iterationen von 2 bis 4 Wochen. Nach jeder Iteration \(auch Sprint genant\), findet ein Release der funktionsfähigen Software statt, welcher getestet und dem Kunden zur Verfügung gestellt werden oder sogar bereits veröffentlicht werden kann.

Dadurch kann der Kunde von Beginn an der Entwicklung des Produktes teilnehmen und aktiv einschreiten. So werden Missverständnisse sehr schnell erkannt und können korrigiert werden.

Wenn wir das Bild oben nochmal betrachten, kann man auf der Fahrradtour mit einer agilen Vorgehensweise jede Etappe separat planen und sich den neuen Gegebenheiten anpassen.

### Iterativ

Die Entwicklung findet in Iterationen / Sprints statt. Die Aktivitäten des Entwicklungszyklus werden in jeder Iteration von neuem durchlaufen. Analyse, Design, Implementierung, Test, Validation, \(Release\).

![](../.gitbook/assets/image%20%28137%29.png)

### Inkrementell

Durch die iterative Vorgehensweise entsteht am Ende jeder Iteration ein Produkt. Die Funktionalität der Software nimmt somit inkrementell zu.

![](../.gitbook/assets/image%20%28151%29.png)



### Vorteile

Wird eine neue Software entwickelt, kann nach jeder Iteration geprüft werden, ob die Software bereits veröffentlicht und kommerziell genutzt werden kann. So kann ein Produkt potentiell viel früher finanzielle Einnahmen generieren und mit den Einnahmen weiterentwickelt werden.

![](../.gitbook/assets/image%20%2898%29.png)

Potentiell hat man in einer agilen Vorgehensweise also schon früher etwas brauchbares und am Ende durch die ständige Reflexion und Überarbeitung vielleicht sogar ein besseres Resultat.

Weitere Vorteile sind:

* Fortlaufendes Kundenfeedback -&gt; verbesserte Kommunikation
* Probleme / Risiken werden früher erkannt
* Greatest Risk first: Reduktion von Projektrisiken: wenn das Projekt scheitert, dann wenigstens früh \(bevor viel Geld ausgegeben wurde\)



## Erfolgreiches Beispiel "Pokemon Go"

Im Sommer 2016 veröffentlichte Nintendo gemeinsam mit Niantic das Smartphone Game "Pokemon Go", wobei die Entwickler agil vorgingen. 

![](../.gitbook/assets/image%20%2843%29.png)

Die erste Version, die im Frühsommer 2016 erschien, war alles andere als "fertig". Viele Features, die beworben wurden, waren gar nicht vorhanden und kamen später mit regelmässigen Software-Updates nach. 

Trotzdem hat das Spiel bereits 30 Tage nach Veröffentlichung 100 Millionen Downloads im Google Play Store verzeichnet und den Entwicklern durch In-App-Käufe rund $160 Millionen eingebracht \(Quelle: [Wikipedia](https://en.wikipedia.org/wiki/Pok%C3%A9mon_Go#Downloads_and_revenue)\).

