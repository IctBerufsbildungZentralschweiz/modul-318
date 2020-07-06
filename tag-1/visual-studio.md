# ❓ Visual Studio & WinForms

## Neue Solution mit Windows Forms Projekt erstellen

* Öffne Visual Studio und erstelle ein neues Projekt.

![](../.gitbook/assets/image%20%2840%29.png)

* Wähle Windows Forms App \(.NET Framework\). 

![](../.gitbook/assets/image%20%2857%29.png)

{% hint style="warning" %}
Wähle **nicht** den Eintrag mit .NET Core, denn das funktioniert nicht \(stand Mai 2020\).
{% endhint %}

{% hint style="info" %}
Falls bei dir kein "Windows Forms App \(.NET Framework\)" erscheint, befolge die Lösung [im FAQ](../faq/#bei-mir-gibt-es-kein-windows-forms-projekt-zur-auswahl).
{% endhint %}

* Gib dem Projekt einen Namen und Klicke auf "Erstellen"

![](../.gitbook/assets/image%20%2893%29.png)



## Windows Forms

Im Visual Studio sollte jetzt die neue Form1 und eine Toolbox ersichtlich sein.

* Wenn die Toolbox nicht aufgetaucht ist, kannst du sie im Menü unter "Ansicht &gt; Toolbox" öffnen.
* Mit der kleinen Pin-Nadel auf der Seite kann die Toolbox geöffnet bleiben, ansonsten klappt sie immer zu.

![](../.gitbook/assets/image%20%2887%29.png)

In der Toolbox befinden sich alle verfügbaren GUI-Elemente. Von hier kann jetzt z.B. ein Button mit Drag'n'Drop auf die Form gezogen werden.

![](../.gitbook/assets/image%20%28171%29.png)

### Element-Eigenschaften

Mit Rechtsklick auf den Button &gt; Eigenschaften erscheint das Eigenschaftenfenster des Buttons.

![](../.gitbook/assets/image%20%2889%29.png)

Das Eigenschaftenfenster sollte geöffnet bleiben. Es zeigt jeweils die Eigenschaften des selektierten GUI-Elements an. Nachfolgend sind einige Eigenschaften eines Elements erläutert:

<table>
  <thead>
    <tr>
      <th style="text-align:left">Eigenschaft</th>
      <th style="text-align:left">Bedeutung</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">(Name)</td>
      <td style="text-align:left">Der Name des Elements, wie es anschliessend im Code verwendet werden kann.
        Dies ist ein Variabelname und sollte entsprechend gut gew&#xE4;hlt werden!</td>
    </tr>
    <tr>
      <td style="text-align:left">Text</td>
      <td style="text-align:left">Der Text, welcher im Element angezeigt wird.</td>
    </tr>
    <tr>
      <td style="text-align:left">Anchor</td>
      <td style="text-align:left">
        <p>Hier kann konfiguriert werden, wie sich das Element bei der Ver&#xE4;nderung
          der Fenstergr&#xF6;sse verh&#xE4;lt.</p>
        <p>
          <img src="../.gitbook/assets/image (69).png" alt/>
        </p>
        <p>Er dockt an einer bestimmten Seite an. Wenn z.B. Links und Rechts ausgew&#xE4;hlt
          sind, vergr&#xF6;ssert sich der Button mit dem Fenster.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TabIndex</td>
      <td style="text-align:left">Dies entscheidet die Reihenfolge des Fokus, wenn der Benutzer in einem
        Textfeld ist und die Tab Taste dr&#xFC;ckt, wird das Feld mit dem n&#xE4;chsth&#xF6;heren
        TabIndex-Wert fokussiert.</td>
    </tr>
  </tbody>
</table>

### Events

Mit einem Klick auf das ![](../.gitbook/assets/image%20%28139%29.png) Icon öffnet sich die Event-Ansicht. Hier sind alle Events aufgelistet, die das gewählte Element aussenden kann, bzw. auf welche wir im Code reagieren können.

![](../.gitbook/assets/image%20%28126%29.png)

Wenn man direkt auf ein Event in dieser Liste doppelklickt, wechselt Visual Studio zur Code-Ansicht und erstellt eine Methode, welche aufgerufen wird, wenn dieser Event ausgelöst wird. Wenn man direkt auf den Button doppelklickt, erstellt Visual Studio eine Methode für den Click-Event.

```csharp
private void button1_Click(object sender, EventArgs e)
{
    
}
```

{% hint style="warning" %}
Wenn man diese Methode im Code löscht, kann man den GUI-Designer nicht mehr öffnen! Man sollte immer zuerst in der Event Liste den Event löschen, danach kann die Methode gelöscht werden.
{% endhint %}

  
Wenn in der Event-Toolbox ein Event ausgewählt wird, steht unten die Erklärung dazu. Hier sind einige wichtige Events aufgeführt:

| Event | Bedeutung |
| :--- | :--- |
| Click | Event, der ausgelöst wird, wenn der Benutzer auf das Element klickt. |
| Enter | Wird ausgelöst, wenn der Fokus in ein Element geht. z.B. Wenn der Cursor \(blinkende Linie im Textfeld\) in ein Textfeld kommt. |
| Leave | Wird ausgelöst, wenn der Fokus aus einem Element verschwindet. |
| KeyUp | Wird ausgelöst, wenn eine Taste auf der Tastatur gedrückt wurde, während der Fokus in diesem Element ist. |
| MouseEnter | Wird ausgelöst, wenn der Mauszeiger sich auf das Element bewegt hat. |
| MouseLeave | Wird ausgelöst, wenn der Mauszeiger das Element verlassen hat. |
| TextChanged | Wird ausgelöst, wenn sich der Text eines Elements geändert hat. |
|  | _und viele mehr..._ |



## 🛠 Beispiel: Hello World

In diesem Beispiel wird Schritt für Schritt beschrieben, wie man ein Hello World programmiert, in welchem "Hello World" in ein Label geschrieben wird, wenn ein Button geklickt wird.

* [ ] Ziehe einen **Button** auf die Form, 
* [ ] Gib ihm den Namen "helloWorldButton" 
* [ ] Gib ihm den Text "Klick Mich!".
* [ ] Ziehe ein **Label** auf die Form.
* [ ] Gib ihm den Namen "ausgabeLabel".
* [ ] Den Text löschst du, sodass nichts im Label steht.

![](../.gitbook/assets/image%20%2844%29.png)

* [ ] Jetzt mache einen Doppelklick auf den "Klick Mich!" Button.

Visual Studio sollte jetzt zur Code-Ansicht wechseln und die folgende leere Methode erstellen:

```csharp
private void helloWorldButton_Click(object sender, EventArgs e)
{

}
```

* [ ] In diese Methode schreibst du jetzt die folgende Codezeile. Dies schreibt den Text "Hello World" in die Text Eigenschaft des Labels `ausgabeLabel` .

```csharp
ausgabeLabel.Text = "Hello World";
```

Das ist schon alles. Starte das Programm, indem du auf den  ![](../.gitbook/assets/image%20%28127%29.png) Button klickst. Probiere es aus!

![](../.gitbook/assets/image%20%28161%29.png)

