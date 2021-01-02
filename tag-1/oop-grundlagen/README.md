---
description: Grundlagen der Objektorientierten Programmierung
---

# 📖 OOP Grundlagen

## 💬 Was ist Objektorientierte Programmierung?

* Wo liegt der Unterschied zur prozeduralen Programmierung?
* Was ist der Unterschied zwischen einer Klasse und einem Objekt?
* Was bewirkt das Schlüsselwort `new` ?
* Was sind Eigenschaften?
* Was sind Methoden?

## Geschichte der Objektorientierung

### Smalltalk

1970 hat Alan Key im XEROX Forschungszentrum die erste OO Sprache "Smalltalk" entwickelt. Sie beeinflusste die Entwicklung vieler späterer Programmiersprachen \(auch Java und C\#\).

Prinzipien von Smalltalk \(und Objektorientierung\):

* Alles ist ein Objekt
* Objekte kommunizieren durch das Senden und Empfangen von Nachrichten
* Objekte haben ihren eigenen Speicherbereich
* Jedes Objekt ist die Instanz einer Klasse.

### ISO Standard

Bereits 1985 wurde die erste Version des ISO/IEC 2382-15 Standards beschrieben. Die aktuellste Version wurde 2015 veröffentlicht.

> Objektorientierung bezieht sich auf eine Technik oder Programmiersprache, welche Objekte, Klassen und Vererbung unterstützt.

Die komplette ISO kann hier gefunden werden: [ISO/IEC 2382-15](https://www.iso.org/obp/ui/#iso:std:iso-iec:2382:ed-1:v1:en)

{% hint style="info" %}
Bernd Oestereich \(Fachbuchautor\):

«Die Objektorientierung heisst Objektorientierung, weil diese Methode die in der realen Welt vorkommenden Gegenstände als Objekte ansieht. Ein Telefon ist genauso ein Objekt wie ein Fahrrad, ein Mensch oder eine Versicherungspolice. Und diese Objekte setzen sich wiederum aus anderen Objekten zusammen, nämlich aus Schrauben, Rädern, Ohren, Tarifen und so weiter.»
{% endhint %}

## Grundlagen & Begriffe

### Objekte und Klassen

<table>
  <thead>
    <tr>
      <th style="text-align:left">Name</th>
      <th style="text-align:left"><b>Objekt</b>
      </th>
      <th style="text-align:left"><b>Klasse</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Beschreibung</b>
      </td>
      <td style="text-align:left">Objekte repr&#xE4;sentieren &quot;Dinge&quot; der realen Welt oder eines
        Problembereichs. Beispiel &quot;der rote Wagen da unten im Parkhaus&quot;.</td>
      <td
      style="text-align:left">Klassen sind Baupl&#xE4;ne f&#xFC;r Objekte. Beispiel &quot;Bauplan f&#xFC;r
        einen Wagen&quot;.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Bild</b>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (1).png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../../.gitbook/assets/image (3).png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>C# Code</b>
      </td>
      <td style="text-align:left"><code>Auto auto = new Auto();</code>
      </td>
      <td style="text-align:left">
        <p><code>public class Auto {</code>
        </p>
        <p> <code>// ...</code>
        </p>
        <p><code>}</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Synonyme</b>
      </td>
      <td style="text-align:left">Instanz</td>
      <td style="text-align:left">Typ, Klassentyp</td>
    </tr>
  </tbody>
</table>

Zwei Autos werden einem Bauplan erstellt, können dann aber unterschiedliche **Eigenschaften** haben \(z.B. Farbe, Geschwindigkeit, usw.\). Genauso können zwei Objekte einer bestimmten Klasse erstellt werden, aber unterschiedliche Eigenschaften haben.

Analogie "Kuchen backen": Ausgehend von einem bestimmten Kuchenrezept \(vgl. Klasse\) lassen sich beliebig viele gleichartige Kuchen \(vgl. Objekte\) backen \(vgl. erzeugen\).

![](../../.gitbook/assets/image%20%28110%29.png)

{% hint style="info" %}
* Wir programmieren Klassen
* Objekte werden ausgehend von Klassen erzeugt und zwar automatisch und erst zur Laufzeit.
* Zur Laufzeit hat man es mit Objekten zu tun, die miteinander interagieren.
{% endhint %}

## Klassendefinition in C\#

Grundaufbau einer Klasse:

{% tabs %}
{% tab title="Beispiel \"Person\"" %}
```csharp
// Klassendefinition
public class Person
{
    // Felder
    private string _name;

    // Eigenschaften
    public string Name { 
        get {
            return _name;
        }
    }
    public DateTime Birthday { get; }

    // Konstruktor ohne Parameter
    public Person()
    {
        Name = "unknown";
    }

    // Konstruktor, der einen Namen und ein Geburtsdatum entgegennimmt
    public Person(string name, DateTime birthday)
    {
        this.Name = name;
        this.Birthday = birthday;
    }

    // Methode, die das aktuelle Alter berechnet.
    public int GetAge() {
        return (new DateTime()).Year - this.Birthday.Year;
    }

    // Methode, die welche die Imlementation der Basisklasse überschreibt.
    public override string ToString()
    {
        return this.Name + " (" + this.GetAge() + ")" ;
    }
}
```
{% endtab %}

{% tab title="Beispiel \"Baum\"" %}
![](../../.gitbook/assets/image%20%2879%29.png)
{% endtab %}
{% endtabs %}

### Konstruktor

Ein Konstruktor ist eine spezielle Methode. Sie wird immer bei der Erzeugung eines Objektes mit dem `new` Keyword aufgerufen.

Dieses Beispiel hat einen Konstruktor ohne Parameter:

```csharp
public class Person
{
    // Eigenschaften
    public string Name { get; }

    // Konstruktor ohne Parameter
    public Person()
    {
        Name = "unknown";
    }
}


Person p1 = new Person();
```

Mithilfe des `new` Keywords wird hier ein neues Objekt der Klasse `Person` erzeugt.

Dieses Beispiel hat einen Konstruktor mit einem Parameter:

```csharp
public class Baum 
{
    private int _hoehe;

    public Baum (int hoehe) {
        this._hoehe = hoehe;
    }
}

Baum b1 = new Baum(55);
```

Hier wird mithilfe des `new` Keywords ein neues Objekt der Klasse `Baum` erzeugt. Dabei wird ein **Parameter** übergeben.

### Attribute

Attribute, auch "Felder" oder "Membervariabeln" genannt, sind Variabeln, welche nur innerhalb des Objektes bekannt sind und auch nur von da verwendet werden sollten. Daher sollten Sie immer mit `private` gekennzeichnet sein.

```csharp
public class Baum 
{
    private int _hoehe;
    // ...
}
```

### Eigenschaften / Properties

Eigenschaften sind \(in der Regel\) nach aussen verfügbar. Im Grunde machen sie Felder nach aussen verfügbar:

```csharp
private string _name;

public string Name { 
    get {
        return _name;
    }
}
```

Eigenschaften bestehen immer aus einem getter und einem setter \(oder nur einem getter, falls es eine readonly-Eigenschaft ist\).

```csharp
public int Alter {
    get {
        // Getter code
    }
    set {
        // Setter code
    }
}
```

Die getter und setter sind quasi eigene Methoden.

In Java beispielsweise gibt es keine Eigenschaften. Da wird jeweils eine Getter-Methode `GetAlter()` und eine Setter-Methode `SetAlter(int alter)`programmiert.

#### Auto-Property

C\# bietet die Möglichkeit sogenannter Auto-Properties. Dies wird dann verwendet, wie im Beispiel oben, wo eine Eigenschaft lediglich als Wrapper eines Feldes dient.

```csharp
// Auto-Property mit Getter und Setter
public string Name { get; set; }

// Read only Auto-Property (nur mit Getter)
public int Alter { get; }
```

{% hint style="info" %}
Der Wert eines Read only Auto-Properties kann nur im Konstruktor gesetzt werden.
{% endhint %}

## Objektinteraktion

Wenn eine Klasse existiert, erstellen wir mittels des `new` Keywords eine Instanz \(also ein Objekt\) dieser Klasse:

```csharp
Person p1 = new Person();
```

Die Eigenschaften und Methoden werden dann mit einem `.` aufgerufen.

```csharp
var alter = p1.Alter;
var asText = p1.ToString();
```

## Vorteile der Objektorientierten Programmierung

### Wiederverwendbarkeit

Klassen modularisieren eine Anwendung in unabhängige Einheiten. Sie verwalten zusammengehörende Daten und gruppieren ähnliche Methoden. Klassen können bausteinähnlich in verschiedenen Programmen – in der .NET-Laufzeitumgebung sogar vollkommen unabhängig von der verwendeten Programmiersprache – gleichwertig eingesetzt werden. Als Konsequenz dessen ändert sich auch der Arbeitsablauf der Programmierung: Programme müssen nicht mehr in allen Einzelheiten neu geschrieben werden, sie werden zu einem großen Teil aus fertigen Komponenten zusammengesetzt – vergleichbar mit der Entwicklung und dem Zusammenbau eines Motors, bei dem im Wesentlichen genormte Maschinenteile \(Schrauben, Bolzen etc.\) zum Einsatz kommen.

### Wartungsaufwand

Eine Klasse kapselt ihre Daten sowie die interne Implementierung ihrer Methoden gegenüber der Aussenwelt und kann daher problemlos an neue Anforderungen angepasst werden. Anwendungsprogramme, welche die Dienste einer Klasse nutzen, bemerken davon nichts. Eine Klasse kann als eigene, separate und unabhängige Einheit getestet werden. Damit ist es auch vollkommen ausreichend, die Klassenimplementierung nur einmal ausgiebig zu testen. Verläuft der Test positiv, wird die Klasse mit jeder Anwendung zufrieden stellend zusammenarbeiten. Das Testen im Umfeld mehrerer Anwendungsprogramme entfällt und stellt damit die Effizienz der Programmierung sicher.

### Fehleranfälligkeit

Die Kapselung bewirkt, dass Objekte den Zugriff auf die Daten selbst kontrollieren und eine fehlerhafte Datenmanipulation und die daraus resultierende Inkonsistenz abwehren können.

## 💡 Kontrollfragen

Versucht zu zweit die Antworten auf die folgenden Fragen zu finden, ohne hoch zu scrollen. Diskutiert eure Antworten und vergleicht sie mit der Antwort, die sich hinter dem Antwort Tab versteckt.

{% tabs %}
{% tab title="Frage" %}
Was ist der Unterschied zwischen einer **Klasse** und einem **Objekt**?

In der Analogie in der Architektur und dem Häuserbau, was wäre da eine Klasse bzw. ein Objekt?
{% endtab %}

{% tab title="Antwort" %}
Die Klasse ist der Bauplan, das Objekt eine einzelne Instanz dieser Klasse.

Die Klasse wäre der Bauplan eines Hauses, das Objekt wäre ein fertig erbautes Haus.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Frage" %}
Was programmiert man als Softwareentwickler? Klassen oder Objekte?
{% endtab %}

{% tab title="Antwort" %}
Klassen.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Frage" %}
Was ist eine Methode?
{% endtab %}

{% tab title="Antwort" %}
Eine Methode ist eine Aktion, welche ein Objekt durchführen kann.
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Frage" %}
Wie erstellt man ein Objekt?
{% endtab %}

{% tab title="Antwort" %}
Mit dem `new` Keyword.
{% endtab %}
{% endtabs %}

