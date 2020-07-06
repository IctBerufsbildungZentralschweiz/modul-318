# ❓Testprotokoll: Praxisbeispiel

## **Testdurchführung 2020-02-26 Sprint 4 - Sprint End Test**

Dokument Version: 1.1  
****Durchführungsdatum: 26.02..2020  
Tester/in: Hans Muster  
App Version & Umgebung: 0.4.0.114 \(DEV\)  
API-Version & Umgebung: 0.4.0.89 \(DEV\)  
&lt;URL&gt; : https://test.pricelist.com:3587/  
  
****

## **Navigation & Sprache**

### **Vorbedingungen**

* Software ist installiert unter &lt;URL&gt;
* Die Folgenden Browser sind auf dem System jeweils in der aktuellsten Version verfügbar:
  * Chrome
  * Edge
  * Firefox

### **Testszenario**

Die Folgenden Schritte mit allen oben genannten Browsern durchführen.  


<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Schritt</b>
      </th>
      <th style="text-align:left"><b>Aktivit&#xE4;t</b>
      </th>
      <th style="text-align:left"><b>Erwartetes Resultat</b>
      </th>
      <th style="text-align:left"><b>Abw. Resultat</b>
      </th>
      <th style="text-align:left"><b>Erf&#xFC;llt</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">Ein Browser Fenster &#xF6;ffnen und &lt;URL&gt; eingeben (ohne &#x2018;/de&#x2019;
        usw.).</td>
      <td style="text-align:left">
        <p>Die eingegebene URL &#xE4;ndert sich zu &#x201C;&lt;URL&gt;/de/pricelist&#x201D;.
          <br
          />
        </p>
        <p>Die Applikation wird auf deutsch angezeigt und die Preisliste wird angezeigt.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">Den Men&#xFC;-Button anklicken.</td>
      <td style="text-align:left">
        <p>Das Men&#xFC; &#xF6;ffnet sich.
          <br />
        </p>
        <p>Es beinhaltet die Abschnitte Preisliste, Produktverwaltung, Partnerverwaltung,
          Sonstiges und unterhalb die Sprachauswahl und die Versionsnummern.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">Bei der Sprachauswahl auf FR klicken.</td>
      <td style="text-align:left">
        <p>Die Seite aktualisiert sich, die URL wechselt auf &#x201C;&lt;URL&gt;/fr/pricelist&#x201D;
          und der Text auf der Seite ist in Franz&#xF6;sisch.
          <br />
        </p>
        <p>(w&#xE4;hrend der Entwicklungsphase ist einiger Text hier noch auf englisch,
          da die Applikation noch nicht auf franz&#xF6;sisch &#xFC;bersetzt wurde).</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Partner Levels&#x201D; navigieren.</td>
      <td style="text-align:left">Die Partner Level Verwaltungsseite &#xF6;ffnet sich, immer noch auf franz&#xF6;sisch.
        Die URL &#xE4;ndert sich zu &#x201C;&lt;URL&gt;/fr/partnerlevels&#x201D;.</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">
        <p>In der Sprachauswahl wieder DE w&#xE4;hlen.
          <br />
        </p>
        <p>(Informelle Zusatztests: Verschiedene Seiten in der Navigation &#xF6;ffnen
          und die Sprache &#xE4;ndern, dabei sollte immer dieselbe Seite ge&#xF6;ffnet
          bleiben und nur die Sprache wechseln.)</p>
      </td>
      <td style="text-align:left">
        <p>Die Seite aktualisiert sich, die URL &#xE4;ndert sich zu &#x201C;&lt;URL&gt;/de/partnerlevels&#x201D;.
          <br
          />
        </p>
        <p>Es ist weiterhin die Partner Level Verwaltungsseite ge&#xF6;ffnet, jetzt
          aber auf deutsch.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Exporte&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite &#x201C;Exporte&#x201D; &#xF6;ffnet sich.</td>
      <td style="text-align:left">Export / Import</td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Produkte&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Produktverwaltung &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Optionen&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Optionenverwaltung &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Preise verwalten&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Preisverwaltung &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Definitionen&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Definitionen &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Preise genehmigen&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Preisgenehmigung &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">11</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Partnerlevels&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Partnerlevels &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">12</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Rabatte&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Rabattdefinitionen &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">13</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Partnerverwaltung&#x201D; klicken.</td>
      <td style="text-align:left">Der Men&#xFC;eintrag kann nicht angeklickt werden, da dieses Feature noch
        nicht umgesetzt ist.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">14</td>
      <td style="text-align:left">Im Men&#xFC; auf &#x201C;Dokumentvorlage&#x201D; klicken.</td>
      <td style="text-align:left">Die Seite der Dokumentvorlage &#xF6;ffnet sich.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;&#x2705;&#x2705;</td>
    </tr>
  </tbody>
</table>

## **Preisliste - Listenansicht**

### **Vorbedingungen**

* Der initiale Import der Daten wurde durchgeführt.
  * Es sind mehr als 50 Produkte vorhanden.
* Rabatte für die Partner Levels wurden definiert.
* Produktbilder wurden für alle Produkte eingestellt.

### **Testszenario**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Schritt</b>
      </th>
      <th style="text-align:left"><b>Aktivit&#xE4;t</b>
      </th>
      <th style="text-align:left"><b>Erwartetes Resultat</b>
      </th>
      <th style="text-align:left"><b>Abw. Resultat</b>
      </th>
      <th style="text-align:left"><b>Erf&#xFC;llt</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">&lt;URL&gt; in einem Google Chrome Fenster &#xF6;ffnen.</td>
      <td style="text-align:left">Die Preisliste &#xF6;ffnet auf deutsch.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">In der Top Bar unter Ansicht auf das Listen-Icon klicken.</td>
      <td style="text-align:left">
        <p>Unterhalb der Top Bar &#xE4;ndert sich die Ansicht zu einer Tabelle mit
          Item-Nr, Name, Bezeichnung, Kategorie und Preis.
          <br />
        </p>
        <p>In der Tabelle werden 10 Eintr&#xE4;ge angezeigt.
          <br />
        </p>
        <p>Unten an der Tabelle wird angezeigt, wie Viele Elemente es total gibt,
          es hat eine Auswahl, um die Anzahl Elemente pro Seite festzulegen und Navigationselemente
          um auf die n&#xE4;chste / vorherige Seite zu wechseln.
          <br />
        </p>
        <p>Die Tabelle ist initial nach Item Nr. sortiert.
          <br />
        </p>
        <p>Oberhalb der Tabelle hat es zwei Tabs f&#xFC;r Produkte und Optionen,
          initial ist das Produkte-Tab ge&#xF6;ffnet.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">Unten an der Tabelle einstellen, dass man 50 Elemente pro Seite sehen
        m&#xF6;chte.</td>
      <td style="text-align:left">Die Tabelle l&#xE4;dt, anschliessend werden 50 Elemente angezeigt.</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">Unten an der Tabelle auf die n&#xE4;chste Seite wechseln.</td>
      <td style="text-align:left">Es werden die n&#xE4;chsten 50 Eintr&#xE4;ge angezeigt. Wenn es insgesamt
        weniger als 100 Eintr&#xE4;ge hat, werden nur die &#xFC;brigen Eintr&#xE4;ge
        ab Nr. 51 angezeigt.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">Im Tabellenheader auf &#x201C;Name&#x201D; klicken.</td>
      <td style="text-align:left">
        <p>Die Tabelle ist jetzt nach Name sortiert, man befindet sich wieder auf
          der ersten Seite.
          <br />
        </p>
        <p>Dabei wird nicht nur die aktuelle Seite neu sortiert, sondern die kompletten
          Daten sortiert.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Oberhalb der Tabelle das Optionen-Tab &#xF6;ffnen.</td>
      <td style="text-align:left">
        <p>In der Tabelle werden nun Optionen angezeigt.
          <br />
        </p>
        <p>Die Anzahl Elemente pro Seite ist wieder auf 10 gestellt</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">6.1</td>
      <td style="text-align:left">Auf einen Eintrag in der Tabelle klicken.</td>
      <td style="text-align:left">In einem Dialog werden die zugeh&#xF6;rigen Produkte angezeigt.</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">Im Tabellenheader auf &#x201C;Optionengruppe&#x201D; klicken.</td>
      <td
      style="text-align:left">
        <p>Die Optionen in der Tabelle sind jetzt nach Optionengruppe sortiert /
          gruppiert.
          <br />
        </p>
        <p>Dabei wird nicht nur die aktuelle Seite neu sortiert, sondern die kompletten
          Daten sortiert.</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">Auf die erste Option in der Tabelle klicken.</td>
      <td style="text-align:left">Nichts passiert.</td>
      <td style="text-align:left">Es &#xF6;ffnet sich ein Dialog in welchem die zugeh&#xF6;rigen Produkte
        von &#x201C;KL3: KYOlife auf 3 Jahre vort Ort, inkl. Optionen&#x201D; angezeigt
        werden</td>
      <td style="text-align:left">&#x1F6AB;</td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">Auf das Tab &#x201C;Produkte&#x201D; wechseln und anschliessend auf das
        erste angezeigte Produkt in der Tabelle klicken.</td>
      <td style="text-align:left">
        <p>In der Top Bar steht nun die Item Nr des angeklickten Produkts in der
          Textsuche.
          <br />
        </p>
        <p>Die Ansicht wurde auf die Detailansicht umgestellt.
          <br />
        </p>
        <p>Auf der Seite wird die Detailansicht des angeklickten Produkts angezeigt.
          Nur dieses Produkt ist sichtbar..</p>
      </td>
      <td style="text-align:left">Es &#xF6;ffnet sich die Preisliste im Tab &#x201C;Produkte&#x201D;. Es
        wird die Listenansicht angezeigt. Das Produkt steht nicht in der Textsuche.</td>
      <td
      style="text-align:left">&#x1F6AB;</td>
    </tr>
    <tr>
      <td style="text-align:left">10</td>
      <td style="text-align:left">In der Top Bar unter Ansicht auf das Listen-Icon klicken und auf das X
        rechts im Suchfeld klicken.</td>
      <td style="text-align:left">Der Text im Suchfeld verschwindet und es werden wieder die Produkte in
        der Tabelle angezeigt.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"><b>&#x2705;</b>
      </td>
    </tr>
  </tbody>
</table>

## **Preisliste - Detailansicht**

### **Vorbedingungen**

* Der initiale Import der Daten wurde durchgeführt.
  * Es sind mehr als 50 Produkte vorhanden.
* Rabatte für die Partner Levels wurden definiert.
  * Für ECOSYS Produkte für das Partner Level “Special” wurde ein Rabatt von 50% festgelegt. ![](https://lh3.googleusercontent.com/MPkh2k1q7YB6VZOJ1HxJnW6fGI-zTX_HVyfV5jJQHBsXH2SFAKSCQ_djz04cL013asegGKTNNSUj4jwwa1S4kWayyJ_8zyjF3MiwvGWmYI_liwgLpubiWB6QjGzPd8z8sJlbwGoI) \(Menü - Rabatte - den Rabatt einstellen\)
* Produktbilder wurden für alle Produkte eingestellt.

### **Testszenario**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Schritt</b>
      </th>
      <th style="text-align:left"><b>Aktivit&#xE4;t</b>
      </th>
      <th style="text-align:left"><b>Erwartetes Resultat</b>
      </th>
      <th style="text-align:left"><b>Abw. Resultat</b>
      </th>
      <th style="text-align:left"><b>Erf&#xFC;llt</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">&lt;URL&gt; in einem Google Chrome Fenster &#xF6;ffnen.</td>
      <td style="text-align:left">
        <p>Die Preisliste &#xF6;ffnet auf deutsch.
          <br />
        </p>
        <p>Es werden 5 Produkte angezeigt.
          <br />
        </p>
        <p>F&#xFC;r jedes Produkt wird Bild, Titel, Untertitel, Beschreibung mit
          roten dreieckingen Auflistungszeichen, Item Nr, Name, Bezeichnung Preis,
          Produktkategorie und Einsatzort angezeigt.
          <br />
        </p>
        <p>F&#xFC;r jedes Produkt sind die dazugeh&#xF6;rigen Optionen nach Optionengruppe
          gruppiert angezeigt sowie deren ItemNr, Name, Bezeichnung und Preis.
          <br
          />
        </p>
        <p>Unten an der Seite wird angezeigt, wie Viele Elemente es total gibt, es
          hat eine Auswahl, um die Anzahl Produkte pro Seite festzulegen und Navigationselemente
          um auf die n&#xE4;chste / vorherige Seite zu wechseln.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">Unten auf der Seite das Pfeil-Icon klicken, um auf die n&#xE4;chste Seite
        zu wechseln. (
        <img src="https://lh4.googleusercontent.com/QqU4P3noE1Lat5XlCPDdyOkRNh_NPyjQlQdZCY9OWE8hMy7BTrb__OqRvPEk1rbd9aqN7DIHw-abiu6Hs-A9hzRZ6Tq8MouwVWCx-8kQQWEzWqllvgt9IlBhAi0YX7jmonXm69ei"
        alt/>)</td>
      <td style="text-align:left">
        <p>Es werden die n&#xE4;chsten 5 Produkte angezeigt.
          <br />
        </p>
        <p>Die Seite scrollt automatisch ganz nach oben.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">3.1</td>
      <td style="text-align:left">Im Suchfeld den Text &#x201C;Standard: Duplexfunktion LCD Display / 5-zeilig&#x201D;
        eingeben</td>
      <td style="text-align:left">
        <p>Die Preisliste aktualisiert und es werden nur noch zwei Produkte angezeigt.
          <br
          />
        </p>
        <p>Damit wird getestet, dass auch die Beschreibung durchsucht wird.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">3.2</td>
      <td style="text-align:left">Auf die Listenansicht wechseln</td>
      <td style="text-align:left">In der Listenansicht wird kein Ergebnis angezeigt, da hier die Beschreibung
        nicht durchsucht wird.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">3.3</td>
      <td style="text-align:left">Zur&#xFC;ck zur Detailansicht wechseln.</td>
      <td style="text-align:left">-</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">Rechts in der Top Bar das Icon f&#xFC;r den erweiterten Filter anklicken
        (
        <img src="https://lh5.googleusercontent.com/3KTpLAVtny58iQX_3yexIxK_07pXX2Gy_VIKRq1_FlS2SR6yEkF1q0CuB7-YbnKsUK47og_3ENvoNKaXB5XHCbKDs90RAW7iMYpMUI_d_iwGkuzdhTR_5ycrcqIYJ0Y643Zf8tGS"
        alt/>).</td>
      <td style="text-align:left">Ein Feld mit dem Titel &#x201C;Filter&#x201D; erscheint. Es beinhaltet
        weitere Filter f&#xFC;r Druckfarbe, Druckformat, Umgebung, Produktkategorie
        und Produktgruppe. Ebenfalls ist ein Reset Button vorhanden (&#x201C;Zur&#xFC;cksetzen&#x201D;).</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">5</td>
      <td style="text-align:left">
        <ul>
          <li>Den Suchtext l&#xF6;schen</li>
          <li>Partnerlevel &#x201C;Special&#x201D; w&#xE4;hlen</li>
          <li>Den erweiterten Filter &#xF6;ffnen, bei Produktgruppe nur &#x201C;ECOSYS&#x201D;
            ausw&#xE4;hlen und den erweiterten Filter wieder schliessen..</li>
          <li>Jetzt bei Preismodell zwischen &#x201C;Verkaufspreis&#x201D; und &#x201C;Partnerpreis&#x201D;
            wechseln.</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Wenn das Preismodell &#x201C;Verkaufspreis&#x201D; gew&#xE4;hlt ist, wird
          als &#xDC;berschrift der Preise &#x201C;VP CHF exkl. MwSt&#x201D; angezeigt.
          <br
          />
        </p>
        <p>Wenn das Preismodell &#x201C;Partnerpreis&#x201C; gew&#xE4;hlt ist, wird
          als &#xDC;berschrift der Preise &#x201C;Ihr Preis CHF exkl. MwSt&#x201D;
          angezeigt. Die Preise f&#xFC;r ECOSYS Produkte sind halb so gross, wie
          unter &#x201C;Verkaufspreis&#x201D;.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">6</td>
      <td style="text-align:left">Im erweiterten Filter den Reset Button klicken.</td>
      <td style="text-align:left">Alle Checkboxen im Filter sind nicht mehr ausgew&#xE4;hlt und es werden
        wieder alle Produkte angezeigt.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">7</td>
      <td style="text-align:left">
        <p>(Informeller Test)</p>
        <p>Die Filter Testen. Checkboxen w&#xE4;hlen und sehen ob die entsprechenden
          Produkte ein / ausgeblendet werden. In der Detailansicht wie auch in der
          Listenansicht testen.
          <br />
        </p>
        <p>Zus&#xE4;tzlich auch das Suchfeld testen.</p>
      </td>
      <td style="text-align:left">Die Seite sollte bei jeder &#xC4;nderung des Filters oder der Suchbox
        sofort aktualisiert werden.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">8</td>
      <td style="text-align:left">
        <p>Folgende Filtereinstellungen w&#xE4;hlen:</p>
        <p>
          <img src="https://lh5.googleusercontent.com/ix0pWtCQbO0Vr6ZlkjLiglhIkcEHEY_WQP6I1r72jeNKBKgocK7d6Ecxl37VcXyKnure9BTylmH4FzXQAXx54eh2wcsRszlBjs1_LNzB2JGOeWFpkRv6KEcIAqG8iVT4T4GMcnUU"
          alt/>
        </p>
      </td>
      <td style="text-align:left">
        <p>Es sollten drei Produkte in der Listenansicht angezeigt werden.
          <br />
        </p>
        <p>In der URL des Browsers sind die Filtereinstellungen sichtbar, etwa so
          (Statt X stehen lange UUIDs):
          <br />
        </p>
        <p>&lt;URL&gt;/de/pricelist?partnerLevelId=X&amp;viewMode=list&amp;priceModel=selling-price&amp;printingColors=X&amp;printingFormats=X&amp;printingEnvironments=X&amp;productCategories=X&amp;productGroups=X</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
    <tr>
      <td style="text-align:left">9</td>
      <td style="text-align:left">Die URL des Browsers kopieren in einem neuen Browserfenster einf&#xFC;gen
        und &#xF6;ffnen.</td>
      <td style="text-align:left">Auf der neu ge&#xF6;ffneten Seite sind dieselben Filtereinstellungen gesetzt
        und die selben Produkte sichtbar.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">&#x2705;</td>
    </tr>
  </tbody>
</table>

