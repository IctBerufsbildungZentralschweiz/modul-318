# ❓ Debugging

Mittels Debugging kannst du die Applikation während des laufenden Betriebs anhalten und Einblick in Variabeln usw. erhalten.

* Klicke neben einer Codezeile auf die graue Fläche, dann erscheint ein roter Kreis, das ist ein Break-Point. Sobald das Programm auf dieser Zeile landet, wird es unterbrochen.

![](../.gitbook/assets/image%20%2852%29.png)

* Starte jetzt das Programm mit dem Start Button.
* Der Break-Point im Beispiel hier ist in der Methode `label1_Click(...)` gesetzt, das heisst, wenn ich auf das label klicke, wird das Programm angehalten.

![](../.gitbook/assets/image%20%284%29.png)

* Visual Studio sollte jetzt so aussehen, auf dem roten Kreis befindet sich jetzt ein gelber Pfeil, dieser zeigt, auf welcher Linie sich die Ausführung des Programms gerade befindet.

![](../.gitbook/assets/image%20%2892%29.png)

* Oben sollten jetzt folgende Schaltflächen auftauchen:

![](../.gitbook/assets/image%20%2874%29.png)

Mit ihnen kann jetzt der Programmablauf gesteuert werden:

* ![](../.gitbook/assets/image%20%28111%29.png) : Stoppt die Ausführung des Programms
* ![](../.gitbook/assets/image%20%2851%29.png) : Stoppt die Ausführung und startet sie erneut.
* ![](../.gitbook/assets/image%20%28130%29.png) : Führt die aktuelle Zeile aus und hält wieder bei der nächsten Zeile.
* ![](../.gitbook/assets/image%20%2813%29.png) : Sprint in eine Anweisung hinein, z.B. bei einem Methodenaufruf springt der gelbe Pfeil in die Methode.
* ![](../.gitbook/assets/image%20%28169%29.png) : Führt den aktuellen Kontext aus und sprint eine Ebene hinaus \(z.B. aus der Methode\) und der gelbe Pfeil springt dort auf die nächste Zeile.
* ![](../.gitbook/assets/image%20%2821%29.png) : Führt das Programm weiter aus \(bis zum nächsten Break-Point\)



Unten im Watcher sieht man die Werte von Variabeln im aktuellen Kontext:

![](../.gitbook/assets/image%20%28142%29.png)



Seitlich in den **Diagnostic Tools** sieht man die aktuelle Auslastung des Speichers und der CPU:

![](../.gitbook/assets/image%20%28173%29.png)

