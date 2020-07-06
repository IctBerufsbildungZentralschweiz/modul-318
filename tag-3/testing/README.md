# 📖 Testing

## Testing

Softwareentwickler sind Menschen und Menschen machen Fehler. So liegt nahe, dass auch jede Software Fehler enthält. Mit Testing-Methoden stellen wir sicher, dass Fehler so früh wie möglich erkannt und behoben werden können.

Es gibt verschiedene Arten, Software zu testen. Manuell, Automatisiert, Black-Box, White-Box Tests. Das Ziel dieser Lektion ist es, die verschiedenen Test-Arten zu kennen und einige davon anwenden zu können.

### 💬 Die Testarten

![](../../.gitbook/assets/image%20%2873%29.png)

Diskutiert gemeinsam in der Klasse:

* Was bedeuten die Einträge in der Testpyramide?
* Was sind Blackbox / Whitebox Tests?
* Welche Einträge in der Pyramide sind Blackbox, welche Whitebox Tests?





## Manuelle Tests

Bei Manuellen Tests handelt es sich meist um Systemtests, da man das komplette System testet.   
Es gibt zwei Arten, eine Software manuell zu testen. Einerseits ist es das informelle Testen, andererseits das formelle Testen. 

Bei einem **Informellen Tests** sitzt jemand vor der Software und probiert die Software aus, gibt schwachsinnige Eingaben ein und versucht so, Fehler in der Software zu finden, ohne einem bestimmten Schema zu folgen.

Bei **formellen Tests** wird vorher in einer **Testplan** Schritt für Schritt niedergeschrieben, was ein Tester klicken und eintippen muss und wie darauf die Software reagieren sollte.

### Testplan

Der Testplan gibt Schritt für Schritt-Anweisungen, welche von der Testenden Person durchgeführt werden sollen. Der Testplan sollte während der Entwicklung wachsen und jeweils neue Testfälle definiert oder Testfälle erweitert werden, damit neue Funktionalität abgedeckt ist.

Ein Testfall besteht immer aus:

* Vorbedingungen
* Testszenario, pro Schritt:
  * Schritt-Id
  * Aktivität
  * Erwartetes Resultat

Siehe hier ein [Beispiel eines Testplans](testplan-beispiel.md)

### Testprotokoll

Das Testprotokoll zeichnet die Durchführung eines Tests durch einen Tester oder eine Testerin auf. Das Testprotokoll ist grundsätzlich eine Kopie des aktuellen Testplans zum Zeitpunkt der Testdurchführung, mit Ergänzung der tatsächlichen Resultate.

Ein Testprotokoll benötigt:

* Dokumentversion \(Testplan\)
* Durchführungsdatum
* Name der testenden Person
* App Version / Umgebung
* Anweisungen, wie auf die Applikation zugegriffen werden kann / wie sie installiert wird.
* Ergänzung jedes Schrittes mit dem Tatsächlichen Resultat und dem Erfüllungsgrad.

Siehe hier ein [Beispiel eines Testprotokolls](testprotokoll-beispiel.md)



## Automatisierte Tests

Im Gegensatz zu manuellen Tests können automatisierte Tests vom Computer selbst und regelmässig durchgeführt werden, z.B. bei jedem Commit & Push.

Automatisierte Tests können auf allen Stufen der Testpyramide vorkommen. Die häufigste Form ist der Unit Test, der jeweils eine individuelle Klasse / Methode Testet.

### Unit Tests

Ein Unit Test ist ein automatisierter Test, welche die kleinste Einheit einer Software testet. Normalerweise gibt es für jede Klasse auch eine Unit Test Klasse und für jede Methode, die getestet wird, mehrere Unit Tests. 

Das Ziel ist es, diese Klasse abgekoppelt von jeglichen Abhängigkeiten testen zu können. 

#### Unit Test Klasse

{% hint style="info" %}
Nach dem AAA-Prinzip wird ein Unit Test mit Kommentaren in drei Bereiche eingeteilt:

* `// arrange`Hier wird alles bereit gemacht, Instanzen erstellt, Werte eingefüllt.
* `// act` Hier wird die Methode aufgerufen, die in diesem Test getestet werden soll.
* `// assert` Hier wird überprüft, ob der Rückgabewert dem erwarteten Ergebnis entspricht.
{% endhint %}

Anschliessend sieht man einen Beispielhaften Unit Test:

```csharp
[TestClass]
public class TransportTest {

  [TestMethod]
  public void TestGetStation() {
    // arrange
    var testee = new Transport();
    
    // act
    var stations = testee.GetStations("luz");
    
    // assert
    Assert.AreEqual(10, stations.StationList.Count);
    Assert.AreEqual("Luzern", stations.StationList[0].Name);
  }
}
```

#### ❓Unit Test erstellen

In einer Visual Studio Solution kann mittels Rechtsklick &gt; Add &gt; New Project &gt; Unit Test Project ein neues Unit Test Projekt hinzugefügt werden. 

Im neu erstellten Projekt kann nun eine neue Klasse erstellt werden nach dem oben abgebildeten Schema.

Um die Tests auszuführen, klickt man im Menü auf Test &gt; Run All Tests.

![](../../.gitbook/assets/image%20%28170%29.png)

### Component, Integration und Systemtests

Component- , Integration- und Systemtests sind ebenfalls automatisiert. Anstatt sich auf eine Klasse zu fokussieren, geht es hier immer mehr auch um das Zusammenspiel mehrerer Klassen, mehrerer Komponenten und auch des kompletten Systems.

### UI Tests

Ein Automatisierter UI Test hat das Potential, je nach Projekt alle manuellen Tests zu ersetzen. Er simuliert einen Tester, der vor dem Programm sitzt und darin Maus- und Tastatureingaben macht und kann überprüfen, ob die Software wie erwartet reagiert.

### Continuous Integration

Da automatisierte Tests ohne menschliche Interaktion durchgeführt werden können, ist es möglich, diese regelmässig durchzuführen. Ein **Build Server** kann beispielsweise bei jedem Commit & Push den neusten Source Code herunterladen und die Unit Tests ausführen.

In einem **Nightly Build** könnte er die automatisierten UI Tests jede Nacht durchführen, weil diese vielleicht etwas länger dauern \(je nach Grösse des Projekts auch einige Stunden\).

![](../../.gitbook/assets/image%20%28134%29.png)





