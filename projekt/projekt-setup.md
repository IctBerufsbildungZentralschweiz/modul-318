# 🛠 Projektsetup

## Repository Forken

Zuerst musst du einen Fork des Repos in deinem eigenen Github Account erstellen. Über diesen Account wirst du das Projekt am Ende des Kurses abgeben.

* Falls du noch keinen github account erstellt hast, erstelle jetzt einen.
* Gehe zur [Projektvorlage](https://github.com/IctBerufsbildungZentralschweiz/modul-318-student) auf Github und erstelle einen Fork in deinen Account:

![](../.gitbook/assets/image%20%28138%29.png)

* Jetzt sollte es automatisch auf das frisch geforkte Projekt in deinem github Profil wechseln. 
* Da klickst du `Clone or download` und anschliessend kopierst du die URL im Textfeld.

![](../.gitbook/assets/image%20%28150%29.png)

## Repository Klonen

Jetzt musst du das Repo auf deinen Rechner klonen, damit du daran arbeiten kannst.

* Öffne jetzt Visual Studio und wähle "Clone or check out code"

![](../.gitbook/assets/image%20%2819%29.png)

* Gib die kopierte URL bei "Repository Location" ein, wähle aus, wo du das Projekt speichern willst und klicke auf "Clone".

![](../.gitbook/assets/image%20%2835%29.png)

## Projekt einrichten

Nach dem Klonen sollte die Solution modul-318-student geöffnet werden. Sie beinhaltet zwei Projekte "SwissTransport" und "SwissTransportTest".

SwissTransport ist das Projekt, welches uns den Zugriff auf die API bietet, um Stationen und Verbindungen aus dem Internet abzufragen.

![](../.gitbook/assets/image%20%2827%29.png)

* Rechtsklicke auf die Solution und wähle "Hinzufügen &gt; Neues Projekt".
* Suche nach "windows forms" und wähle "**Windows Forms App \(.NET Framework\)**". 

![](../.gitbook/assets/image%20%28119%29.png)

{% hint style="danger" %}
Wähle nicht den Eintrag mit .NET Core, denn das funktioniert nicht.
{% endhint %}

* Gib dem Windows Forms Projekt einen sinnvollen Namen, z.B. "MyTransportApp" und klicke auf Create.
* Jetzt sollten in deiner Solution drei Projekte angezeigt werden.
* Damit das neu erstellte Projekt das Startprojekt ist, rechtsklicke auf dein neu erstelltes Projekt und wähle "Als Startprojekt festlegen". Anschliessend sollte es Fett geschrieben sein:

![](../.gitbook/assets/image%20%2875%29.png)

Als nächstes müssen wir eine Referenz zum SwissTransport Projekt erstellen, damit wir auf Klassen dieses Projekts zugreifen können.

* Rechtsklicke dazu auf "References" unter deinem Projekt und "Add Reference"
* Hier wählst du nun "SwissTransport" an und klickst OK.

![](../.gitbook/assets/image%20%2894%29.png)



* Fahre auf der nächsten Seite fort, um den ersten Commit und Push durchzuführen.

