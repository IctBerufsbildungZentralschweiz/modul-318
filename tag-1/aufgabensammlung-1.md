# 💡📖 Aufgabensammlung

## Info

Unten stehen sechs Aufgaben. Es ist empfohlen, dass alle Aufgaben in der selben Projektmappe \(Solution\) gelöst werden. In der Projektmappe soll pro Aufgabe ein Projekt angelegt werden. Du kannst wählen, welches Projekt ausgeführt wird, indem du folgenden Anweisungen folgst: [❓FAQ](../faq/#wie-kann-ich-waehlen-welches-meiner-projekte-ausgefuehrt-wird) \(Wie kann ich wählen, welches meiner Projekte ausgeführt wird?\).

## Aufgabe 1

### Themen

* TextBox Control
* Button Control
* ListBox Control

![Beispiel Aufgabe 1](../.gitbook/assets/image%20%2846%29.png)

Es soll ein Text eingegeben werden können. Dieser Text wird der Liste hinzugefügt, sobald die Eingabe bestätigt wird. Die Listeneinträge sollen nummeriert werden \("1: \_", "2: \_", ...\).

{% hint style="info" %}
* Die Controls verwenden, welche bei Themen genannt werden.
* "+"-Operator für das Verknüpfen von Strings verwenden \(siehe Code unten\)
{% endhint %}

```csharp
var name = "Bob";
var text = "Name: " + name;
// => text == "Name: Bob"
```

## Code-Qualität

### Themen

* Namensgebung
* Angenehme Benutzeroberfläche gestalten

Folgendes soll bei der **generellen** **Namensgebung** beachtet werden:

* Priorisiere Lesbarkeit über Kürze \(CanScrollHorizontally anstatt ScrollableX\)
  * Auch keine Abkürzungen, ausser in Ausnahmefällen mit allgemein bekannten Abkürzungen
* Wähle eine einfache Reihenfolge \(CanScrollHorizontally anstatt HorizontalCanScroll\)
* Gestalte den Namen einfach
  * Keine \_ und andere Sonderzeichen
  * Keine Typ-Prefixe \(name anstatt sName\) \(Ausnahme siehe Controls\)
  * Keine Umlaute

Folgendes soll bei der **Namensgebung für WinForms** beachtet werden:

* Projektmappen sollen sinnvolle Namen haben \(z.B. "M318Exercises" anstatt "MySolution"\)
* Projekte sollen sinnvolle Namen haben \(z.B. "M318Exercise1" anstatt "MyFormsProject"\)
  * Der Name kann auf Deutsch oder Englisch sein, solange alle Namen in **derselben** Sprache sind.
  * _Optional_: Der Name kann Punkte enthalten. Wenn er Punkte enthält, soll der Namen der Projektmappe am Anfang des Namens des Projekts stehen \(z.B. "_M318.Exercises_" & "_M318.Exercises_.Nr1"\) Stichwort: [Namespaces](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/).
* Die Controls \(z.B. Label, TextBox, ListBox\) sollen sinnvolle Namen haben
  * Beispiel 1: titleLabel anstatt label1
  * Beispiel 2: connectionsGrid anstatt dataGridView1 oder connectionsDataGridView
  * Wichtig: Alle Controls sollen gute Namen haben, nicht nur die, welche im Code verwendet werden.
* Die Events sollen sinnvolle Namen haben
  * Option 1: Korrekte Namensgebung verwenden
    * \_ entferenen
    * Umformulierung
    * Beispiel: ConnectionsSelectedIndexChanged
  * Option 2: Generierte Namen verwenden
    * Achtung: Wenn ein Control umbenennt wird, müssen auch die dazugehörigen Events umbenennt werden.
    * Beispiel: connectionsGrid\_SelectedIndexChanged

Folgendes soll Für die **Benutzerfreundlichkeit** beachtet werden:

* Die Tab-Reihenfolge soll sinnvoll sein
  * TabIndex-Eigenschaft
  * Zusammengehörige Controls nacheinander
  * Etwa in der Reihenfolge, wie man liest
* Bestätigungsfunktion \(AcceptButton-Eigenschaft von Form\)
  * Stellt ein, was passiert, wenn man Enter drückt
  * Sollte beinahe immer gesetzt sein
* Abbrechenfunktion \(CancelButton-Eigenschaft von Form\)
  * Stellt ein, was passiert, wenn man Escape drückt
  * Soll bei Dialogen gesetzt sein
* Anchoring korrekt gesetzt
  * Wenn man bei einem Form die Grösse verändern kann, muss die Anchor-Eigenschaft der Controls gesetzt werden. So werden die Controls sauber angezeigt.
  * Tipp: Controls, welche den Anchor links haben, sollen nur links von Controls sein, welche den Anchor rechts haben. Controls, welche den Anchor sowohl links als auch rechts haben, soll rechts nur rechts-Anchored und links nur links-Anchored Controls haben.

Folgendes sollte zur **allgemeinen Codequalität** beachtet werden:

* Magic Strings: Strings, welche direkt in einer Statement hart kodiert sind und das Verhalten der Anwendung steuern. Diese sollen via Konstanten oder Variablen abgebildet werden. Mehr, siehe: [https://deviq.com/magic-strings/](https://deviq.com/magic-strings/)
* Redundante Strings: Wenn ein String doppelt in der Anwendung vorkommt soll er via Konstanten oder Variablen ausgelagert und nur einmalig deklariert werden. Dies gilt doppelt für Magic Strings.
* Die Einrückung soll immer gleich sein \(Standard im Visual Studio: 4 Tabs pro geschachteltem Codeblock\)

Diese Grundsätze sollen ab jetzt immer umgesetzt werden. Bei der Projektarbeit zählt das zu Benutzerfreundlichkeit und Code-Qualität!

## Aufgabe 2

### Themen

* ComboBox Control
* Buttons korrekt einschalten oder ausschalten
* Doppelklick

![Beispiel Aufgabe 2](../.gitbook/assets/image%20%28149%29.png)

Erstelle eine Anwendung, in welcher du auswählen kannst, was du frühstücken möchtest. Diese Anwendung soll aus folgenden Teilen bestehen:

* Combobox, welche alle nicht gewählten Nahrungsmittel enthält
* Listbox, welche die gewählten Nahrungsmittel enthält
* Ein Button "&gt;&gt;", welcher das in der Combobox markierte Nahrungsmittel wählt
* Ein Button "&lt;&lt;", welcher das in der Listbox markierte Nahrungsmittel entwählt

Ein Doppelklick auf ein Nahrungsmittel in der Listbox hat dieselbe Funktionalität wie der Button "&lt;&lt;", das Nahrungsmittel soll also entwählt werden.

Ein wichtiges Feature ist, dass die Buttons korrekt ein- und ausgeschalten werden. Wichtig zu beachten ist, dass jedes Nahrungsmittel entweder in der Combobox oder in der Listbox ist, aber nicht an beiden Orten zugleich.

{% hint style="info" %}
* Korrekt ein- und ausschalten bedeutet, dass die Buttons nur dann eingeschaltet sein dürfen, wenn das dazugehörige Control ein Nahrungsmittel markiert hat. Beispiel: "&gt;&gt;" darf nur eingeschaltet sein, wenn in der ComboBox ein Nahrungsmittel markiert ist. 
{% endhint %}

## Aufgabe 3

### Themen

* RadioButton Control
* CheckBox Control
* GroupBox Control

![Beispiel Aufgabe 3](../.gitbook/assets/image%20%28164%29.png)

Erstelle eine Anwendung mit drei Gruppen \(GroupBox\). In der ersten zwei Gruppen sollen je drei RadioButton-Controls sein. In der dritten Gruppe sollen drei CheckBox-Controls sein. Beim Klick auf einen Button soll eine MessageBox gezeigt werden, welche ausgibt, was ausgewählt wurde.

{% hint style="info" %}
* Falls du nur einen RadioButton auf dem ganzen Form anwählen kannst, liegt es wohl an der GroupBox
* MessageBox.Show\(\) oder MessageBox.ShowDialog\(\) um eine solche anzuzeigen
* Für schnelle:
  * Mit GroupBox.Controls kann man auf die Buttons und Boxes zugreifen
  * Mit [List&lt;T&gt;.OfType\(\)](https://docs.microsoft.com/en-us/dotnet/api/system.linq.enumerable.oftype) kann man eine Liste nach Typ filtern
{% endhint %}

## Aufgabe 4

### 4.1

#### Themen

* Eingabevalidierung
* Status der Anwendung merken

![Beispiel Aufgabe 4.1](../.gitbook/assets/grafik%20%288%29.png)

Erstelle ein Form, welches ein Eingabefeld, einen Einzahlen-Button, einen Abheben-Button und ein Label mit dem aktuellen Kontostand hat. Man darf nur positive Zahlen eingeben. Das Abheben soll nur dann passieren, wenn man auch genügend Geld auf dem Konto hat. Ansonsten soll eine Fehlermeldung gezeigt werden. Die Anzeige soll immer den aktuellen Kontostand anzeigen.

### 4.2

#### Themen

* DataGridView Control

![Beispiel Aufgabe 4.2](../.gitbook/assets/grafik%20%282%29.png)

Neu soll ein Protokoll erstellt werden. Verwende dafür eine DataGridView mit drei Spalten: Uhrzeit, Änderung des Kontostands und neuer Kontostand. 

{% hint style="info" %}
* Die DataGridView ist ein nützliches Control
* [Siehe FAQ](../faq/winforms-data-grid.md)
{% endhint %}

### 4.3

#### Themen

* Logik in eine Klasse auslagern

Erstelle eine Klasse, welche die Logik für dein Bankkonto enthält. Sie soll folgende Methoden enthalten:

```csharp
public class BankAccount // Oder ‘Bankkonto’, je nach gewählter Sprache
{
    public decimal Balance { get; private set; }
    public bool Deposit(decimal amount) {...}
    public bool Withdraw(decimal amount) {...}
}
```

Lagere nun alle Logik in diese Klasse aus. Beachte, dass du keine redundante Logik hast. Die Klasse soll für alle möglichen Eingaben korrekt reagieren, sprich negative Eingaben ablehnen.

### 4.4

#### Themen

* Datei-Interaktionen

Der aktuelle Kontostand soll nun nicht nur angezeigt, sondern auch in einer Datei gespeichert werden. Wenn die Anwendung gestartet wird soll der Kontostand aus der Datei geladen werden. Diese Datei soll im Ordner der Temporären App-Daten sein \(Umgebungsvariable %TEMP%\).

{% hint style="info" %}
* Baue diese Logik in die bei 4.3 erstellte Klasse ein
* File.ReadAllText\(\) um den ganzen Text einer Datei zu lesen
* File.Exists\(\) um zu überprüfen, ob eine Datei existiert
* Für schnelle:
  * Streams sind eine robuste Alternative zur File-Klasse, die ihr wahrscheinlich noch antreffen werdet. Hier wäre eine Gelegenheit, das einzubauen. Siehe [Dokumentation dazu](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-read-text-from-a-file).
{% endhint %}

## Aufgabe 5

### Themen

* Timer
* Anwendung mit mehreren möglichen Stati abbilden

Entwickle eine Stoppuhr. Sie soll aus einer Zeitanzeige \(hh:mm:ss\), zwei Buttons und einer ListBox bestehen. Sie soll den folgenden Ablauf abbilden können:

![Ausgangslage](../.gitbook/assets/grafik%20%2822%29%20%281%29.png)

![Stoppuhr l&#xE4;uft](../.gitbook/assets/grafik%20%287%29.png)

![Runden werden erfasst](../.gitbook/assets/grafik%20%2811%29.png)

![Stoppuhr wird angehalten](../.gitbook/assets/grafik%20%2819%29.png)

![Stoppuhr wird in die Ausgangslage zur&#xFC;ck gesetzt](../.gitbook/assets/grafik%20%2822%29.png)

{% hint style="info" %}
* Benenne die zwei Buttons mit einem sinnvollen Namen. Dies ist besonders wichtig, weil sich der Text ändern kann und die Buttons mehere Funktionen haben.
* Schaue die Timer-Komponente \(Toolbox &gt; Timer, genannt System.Windows.Forms.Timer\) an. Kann diese eine Lösung sein?
* `System.TimeSpan` kann für Zeitdauern verwendet werden und `DateTime.Now` liefert das aktuelle Datum mit Uhrzeit
* Beachte, dass Runden unterbrochen werden können und noch immer die richtige Zeit haben müssen.
* Schaue genau, ob deine Sekunde eine Sekunde lang ist. Es ist einfach, hier und da ein paar Millisekunden zu verlieren.
{% endhint %}

## Aufgabe 6

### Themen

* Komplexere Anwendung realisieren

Erstelle eine Adressverwaltung. Die wichtigsten Funktionen sind:

* Erfassen, Löschen und Bearbeiten von Adressen
* Speichern und Laden der Adressen in/aus einer Datei
* Suchen von Adressen

Anforderungen:

* Klasse, z.B. Address, welche die Daten einer Adresse enthält. Sie soll folgende Eigenschaften haben:
  * Vorname
  * Nachname
  * Strasse
  * Postleitzahl
  * Ort
* UI
  * Suchfeld
  * DataGridView mit der Liste der Adressen
  * Eingabefelder für die Eigenschaften der neuen oder zu bearbeitenden Adresse
  * Toolbar mit einer Option "Datei" mit den Optionen "Speichern" und "Laden"
* Die Suche soll alle Eigenschaften der Adresse beinhalten.
* Das Speichern und Laden der Adressen in einer Datei soll nur via Optionen in der Toolbar passieren, nicht beim Start der Anwendung.
* Das Datei für das Speichern und Laden soll mit einem Datei-Dialog gewählt werden können.

