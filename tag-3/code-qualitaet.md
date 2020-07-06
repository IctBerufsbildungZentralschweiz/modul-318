# 📖 Code Qualität

## 💬 Klassendiskussion

Besprecht gemeinsam in der Klasse:

* Wie bekomme ich Qualität in den Code?
* Warum wollen wir Qualität?
* Was heisst Qualität?



## Externe Qualität vs interne Qualität

<table>
  <thead>
    <tr>
      <th style="text-align:left">Externe Qualit&#xE4;t</th>
      <th style="text-align:left">Interne Qualit&#xE4;t</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <img src="../.gitbook/assets/image (63).png" alt/>
      </td>
      <td style="text-align:left">
        <img src="../.gitbook/assets/image (20).png" alt/>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Was der User sieht.</p>
        <ul>
          <li>Features</li>
          <li>Performance</li>
          <li>Look &amp; Feel</li>
          <li>Zuverl&#xE4;ssigkeit</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Unter der Motorhaube.</p>
        <ul>
          <li>
            <p>Art und Weise, wie Subsysteme, Komponenten, Klassen, Methoden usw. gebaut
              und programmiert sind</p>
            <p></p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

Die Interne Qualität beeinflusst die externe Qualität. Wenn beispielsweise der Motor eines Autos aufgrund von Qualitätsproblemen \(interne Qualität\) nicht mehr läuft, fährt es auch nicht mehr von A nach B. Hat eine Software schlechte interne Qualität, kann das nach extern mehr Kosten verursachen, da es vielleicht schwer erweiterbar ist, früher abgelöst werden muss etc.

➔ Schlüsselfaktor Interne Qualität!



## Qualität messen

### Externe Qualität messen

Funktionierende Software \(Korrektheit\):

* Die Software tut, was sie soll.
* Performance ist akzeptabel
* User Experience / Usability

Die externe Qualität kann hauptsächlich mittels [Testing](testing/) überprüft werden, was später im Kurs noch behandelt wird.

### Interne Qualität messen

Code veränderbar halten:

* Readability
* Simplicity
* Testability

![](../.gitbook/assets/image%20%285%29.png)

### Evolvierbarkeit

Damit Änderungen möglich sind, muss die Software eine innere Struktur haben, die solche Änderungen begünstigt. Dies bezeichnen wir als Evolvierbarkeit. Software wird in der Regel über lange Zeiträume betrieben. Während dieser Zeit ändern sich die Rahmenbedingungen, müssen Features ergänzt werden. Im Idealfall kostet die Implementierung eines Features einen festen Betrag, der unabhängig davon ist, wann das Feature realisiert wird.

Oft ist es auch heute noch so, dass in der Praxis der Preis für ein Feature steigt, je später es realisiert wird. Am Anfang sind Features preiswert, am Ende ist es teilweise gar nicht mehr möglich Features zu ergänzen, weil niemand mehr durchblickt. Die Software wird weggeworfen und neu entwickelt. Bis man an diesem Punkt ankommt, steigen die Kosten exponentiell. Das gemeine an exponentiellem Wachstum sind zwei Dinge: 

1. Anfangs erkennt man kaum, dass die Kosten anwachsen. Die Steigerungen sind moderat. 
2. Wenn man dann erkennt, dass die Kosten steigen, ist es zu spät. Die Steigerung schreitet dann plötzlich so schnell voran, dass ein Gegensteuern nicht mehr möglich ist.

Je einfacher die Software an geänderte Rahmenbedingungen angepasst werden kann, desto höher ist ihre Evolvierbarkeit. Doch Evolvierbarkeit erhält man nicht nachträglich. Evolvierbarkeit muss von Anfang an berücksichtigt werden!  Die Software muss darauf ausgelegt sein.

### Korrektheit

Software muss funktional korrekt sein. Ein Buchhaltungsprogramm muss die Buchungen ordnungsgemäss verbuchen, eine Tabellenkalkulation muss richtig rechnen. Und auch die nicht-funktionalen Anforderungen müssen erfüllt sein. Das Programm muss schonend mit Ressourcen wie Speicher, Prozessorzeit, Plattenplatz, etc. umgehen, die Antwortzeiten müssen in einem definierten Rahmen liegen. Erst wenn alle Anforderungen erfüllt sind, ist die erstellte Software korrekt.

Dass Korrektheit erforderlich ist, wird niemand bestreiten. Doch die Frage ist, was konkret dafür getan wird. Es reicht unserer Ansicht nach nicht aus, Software nach deren Erstellung durch eine Testabteilung zu leiten, deren Aufgabe es ist, Fehler zu finden. Wir meinen, Korrektheit muss bereits während der Entwicklung berücksichtigt werden. Bereits die Entwickler müssen sich mit der Frage der Korrektheit auseinandersetzen. Und damit sie das überhaupt können, muss ihnen klar sein, was die Anforderungen sind. Schon daran mangelt es zu oft! Entwickler werden beauftragt, ein Feature zu implementieren, ohne ihnen präzise zu sagen, was die Abnahmekriterien für das Feature sind. Doch hier geht es nicht darum, Schwarzer Peter zu spielen und einen Schuldigen außerhalb der Entwicklungsabteilungen zu suchen. Schließlich ist es die Aufgabe der Entwickler, bei unklaren Anforderungen nachzufragen, statt in ihre Glaskugel zu schauen.



## Qualität erreichen

Um Software in guter Qualität zu schreiben, sind drei Schlüsselfaktoren sehr wichtig: Fokus, Qualität regelmässig messen und gute Teamarbeit.

### Fokus

* Auf einzelnen Task konzentrieren.
* Klares Ziel und klare Anforderungen - sonst wird falsches gebaut.
* Abschluss des Tasks in Sichtweite, Tasks von kleiner [Granularität](../tag-2/analyse-and-design.md#granularitaet).

### Qualität regelmässig messen

* Regelmässiges Messen der Qualität führt zu guter Qualität am Ende.
* Reflexion: Ohne Rückschau ist keine Weiterentwicklung möglich. Nur wer reflektiert, wie er eine Aufgabenstellung gelöst hat, kann feststellen, ob der gewählte Weg einfach oder beschwerlich war.
* Neue Erkenntnisse berücksichtigen: In einer jungen Wissenschaft wie der Informatik ist es wichtig, stets neue Erkenntnisse zu berücksichtigen. Dazu ist Reflexion auf allen Ebenen erforderlich. Angefangen beim Reflektieren über die Implementation beim Pair Programming oder Code Review, das tägliche Reflektieren des Teams, die Reflexion nach jeder Iteration, bis hin zur Reflexion der gesamten Branche über ihr Tun. Ohne Reflexion keine Weiterentwicklung!

### Teamarbeit

* Team nach Fähigkeiten aufstellen und diese Fähigkeiten bewusst nutzen \(UI, Database, Multi-Threading, Kommunikation, Testing, Automation, Prozess, Social Skills usw.\)
* Spezialisten arbeiten als Team
* Darauf achten, dass keine Tätigkeit nur von einem einzigen Teammitglied abhängig ist -&gt; Bottleneck, wenn Spezialist nicht verfügbar, überlastet  oder vom Zug überrollt wurde.
* Versuchen, T-Shaped Personen aufzubauen \(spezialisiert in einem Bereich, generalisiert auf vielen Gebieten\)



## Clean Code

![](../.gitbook/assets/image%20%28112%29.png)

Die Clean Code Prinzipien leiten  Clean Code Developer in ihrer täglichen Arbeit!

Das mag sich nun in der Kürze etwas antiquiert oder sektiererisch anhören. Sollen Softwareentwickler sich eine Zunftordnung geben oder gar einen Treueeid schwören? Nein, so meinen wir es natürlich nicht. Dennoch: In Ermangelung eines Konsenses darüber, was denn genau „gute Softwareentwicklung“ sei, glauben wir, dass ein „kleinster gemeinsamer Nenner“ Not tut. Die Branche – wobei wir hier zunächst nur die .NET Softwareentwicklung meinen – braucht einen Qualitätsmaßstab oder zumindest einen Erwartungshorizont für Professionalität. Die Zeiten, in denen jeder, der schon mal etwas in BASIC programmiert hatte, ausreichend qualifiziert war, um in einem Team mitzuarbeiten, sind vorbei. Genauso ist aber noch nicht die Zeit gekommen, in der die Vorlage eines Informatik Diploms wirklich etwas über die Befähigung zur Softwareentwicklung aussagen würde.

Wer nicht das ganze Buch lesen möchte, kann mal mit dem Cheat Sheet beginnen, welches die Wichtigsten Prinzipien und Praktiken abbildet:

{% file src="../.gitbook/assets/v2\_clean\_code\_v3.pdf" caption="Clean Code Cheat Sheet \(BBV\)" %}

Nachfolgend werden ein paar Beispiele abgehandelt.

### Loose Coupling

Zwei Klassen, Komponenten oder Module sind gekoppelt, wenn wenigstens einer den anderen verwendet. Umso weniger Abhängigkeiten zwischen den Elementen bestehen, desto weniger sind sie gekoppelt.

Eine Komponente, die lose gekoppelt ist, kann viel einfacher geändert oder ausgetauscht werden, als eine stark gekoppelte Komponente.

### Naming 

#### Choose Descriptive / Unambiguous Names

Namen müssen abbilden, wofür eine Variable, eine Eigenschaft oder eine Klasse abbildet. Namen müssen präzise sein!

#### Name Methods After What They Do

Der Name einer Methode muss beschreiben, was sie macht, nicht wie sie es macht.

#### Name Describe Side Effects

Namen müssen die komplette Funktionalität reflektieren.

#### NO Encoding in Names

Keine Präfixes \(wie `m_Variable`\), keine Typeninformationen \(wie `string sName` \).

### Pair Programming

Zwei Entwickler lösen ein Problem gemeinsam an einem Arbeitsplatz. Jemand ist der Fahrer, der andere der Navigator. Der Fahrer ist verantwortlich dafür, den Code zu schreiben, der Navigator ist verantwortlich, die Lösung an die Architektur und die Coding Richtlinien zu halten und schaut, wo es als nächstes hin geht. Beide fordern ihre Ideen und Herangehensweisen heraus.

### Test Driven Development \(TDD\)

> Red – green – refactor. Test a little – code a little.

TDD ist ein Prinzip, in welchem man wann immer möglich zuerst einen Test programmiert und erst anschliessend die Funktionalität. Hier sprechen wir von sehr kleinen Schritten mit etwas Test-Code und etwas Production Code.

### Pfadfinderregel

![](../.gitbook/assets/image%20%28148%29.png)

