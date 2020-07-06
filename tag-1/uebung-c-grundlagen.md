---
description: 'Einführung in C# und die Grundlagen dieser Programmiersprache.'
---

# 💡 Übung C\# Grundlagen

Es ist am einfachsten, Notizen auf einem Blatt Papier zu machen, um die Aufgaben zu lösen.   
Du kannst den Code zum Verständnis auch ins Visual Studio kopieren, versuch's doch zuerst auf Papier 😉

### Aufgabe 1

{% tabs %}
{% tab title="Aufgabe" %}
Was ist der Wert der Variablen `i` und `a`  nach Durchlauf des Code-Abschnittes?  

```csharp
int i = 0; 
int a = 2; 

i = a++;
```
{% endtab %}

{% tab title="Lösung" %}
Was ist der Wert der Variablen `i` und `a`  nach Durchlauf des Code-Abschnittes?

```csharp
int i = 0; 
int a = 2; 

i = a++;
```

#### Lösung

Da bei `a++` zuerst die Zuweisung zu `i` und erst danach das Inkrementieren gemacht wird, ist die Lösung:

```csharp
i = 2
a = 3
```

{% hint style="info" %}
Wäre der Ausdruck stattdessen `i = ++a` gewesen, wären beide `3` gewesen, denn da passiert zuerst das Inkrementieren.
{% endhint %}
{% endtab %}
{% endtabs %}

### Aufgabe 2

{% tabs %}
{% tab title="Aufgabe" %}
Was ist der Wert der Variablen `i` und `c`  nach Durchlauf des Code-Abschnittes?

```csharp
int i = 0;
int c;

for (c = 1; c <= 4; c++) {
    i += c - 0; 
}
```
{% endtab %}

{% tab title="Lösung" %}
Was ist der Wert der Variablen `i` und `c`  nach Durchlauf des Code-Abschnittes?

```csharp
int i = 0;
int c;

for (c = 1; c <= 4; c++) {
    i += c - 0; 
}
```

#### Lösung

```csharp
i = 10
c = 5
```

Siehe Tab "Lösungsweg" für weitere Details zum Lösungsweg.
{% endtab %}

{% tab title="Lösungsweg" %}
#### Lösungsweg

![](../.gitbook/assets/image%20%28152%29.png)

![](../.gitbook/assets/image%20%2854%29.png)

![](../.gitbook/assets/image%20%28166%29.png)

![](../.gitbook/assets/image%20%28114%29.png)

![](../.gitbook/assets/image%20%28108%29.png)

![](../.gitbook/assets/image%20%2831%29.png)

![](../.gitbook/assets/image%20%28101%29.png)

![](../.gitbook/assets/image%20%2811%29.png)

![](../.gitbook/assets/image%20%28147%29.png)

![](../.gitbook/assets/image%20%2824%29.png)

![](../.gitbook/assets/image%20%2888%29.png)

![](../.gitbook/assets/image%20%2838%29.png)

![](../.gitbook/assets/image%20%28172%29.png)

![](../.gitbook/assets/image%20%2837%29.png)

![](../.gitbook/assets/image%20%28141%29.png)

![](../.gitbook/assets/image%20%28116%29.png)

![](../.gitbook/assets/image%20%2853%29.png)
{% endtab %}
{% endtabs %}

### Aufgabe 3

{% tabs %}
{% tab title="Aufgabe" %}
Was ist der Wert der Variablen `b` , `m` und `n`  nach Durchlauf des Code-Abschnittes?  

```csharp
int n, m;
bool b;
n = 0;
m = 1;
b = true;

while (b && n < m) {
    ++n;
    ++m;
    if (n == 20)
    {
        n++;
    }
    if (m == 22)
    {
        b = false;
    }
}
```
{% endtab %}

{% tab title="Lösung" %}
Was ist der Wert der Variablen `b` , `m` und `n`  nach Durchlauf des Code-Abschnittes?  

```csharp
int n, m;
bool b;
n = 0;
m = 1;
b = true;

while (b && n < m) {
    ++n;
    ++m;
    if (n == 20)
    {
        n++;
    }
    if (m == 22)
    {
        b = false;
    }
}
```

#### Lösung

```csharp
b = true
m = 21
n = 21
```

{% hint style="info" %}
Der Ausdruck `(b && n < m)` ist true wenn `b == true` ist UND `n < m` ist. Also wenn beide Bedingungen zutreffen.

Die `while` Schlaufe wird solange ausgeführt, wie der Ausdruck `true` ist.
{% endhint %}
{% endtab %}
{% endtabs %}

### Aufgabe 4

{% tabs %}
{% tab title="Aufgabe" %}
Was ist der Wert der Variabel `i`  nach Durchlauf des Code-Abschnittes?  

```csharp
int i = 10;
while (true)
{
    if (i != 9)
    {
        i += 2;
        break; 
    }
}
```
{% endtab %}

{% tab title="Lösung" %}
Was ist der Wert der Variabel `i`  nach Durchlauf des Code-Abschnittes?  

```csharp
int i = 10;
while (true)
{
    if (i != 9)
    {
        i += 2;
        break; 
    }
}
```

#### Lösung

```csharp
i = 12;
```

{% hint style="info" %}
Der Ausdruck `i != 9` ist gleich zu Beginn wahr, `i` wird um 2 erhöht und mittels `break` wird die `while` Schlaufe beendet.
{% endhint %}
{% endtab %}
{% endtabs %}

### Aufgabe 5

{% tabs %}
{% tab title="Aufgabe" %}
Was ist der Wert der Variabel `j`  nach Durchlauf des Code-Abschnittes?  

```csharp
int j = 0; 
int i = 2; 

switch (i) {
    case 1:
        j = 1;
        break;
    case 2:
    case 3:
        j = 3;
        break;
    case 4:
        j = 4;
        break;
    default:
        j = 100;
        break; 
}
```
{% endtab %}

{% tab title="Lösung" %}
Was ist der Wert der Variabel `j`  nach Durchlauf des Code-Abschnittes?  

```csharp
int j = 0; 
int i = 2; 

switch (i) {
    case 1:
        j = 1;
        break;
    case 2:
    case 3:
        j = 3;
        break;
    case 4:
        j = 4;
        break;
    default:
        j = 100;
        break; 
}
```

#### Lösung

```csharp
j = 3;
```
{% endtab %}
{% endtabs %}

### Aufgabe 6

{% tabs %}
{% tab title="Aufgabe" %}
Was ist jeweils der Wert der Variable `b`  nach Durchlauf des Code-Abschnittes?  

```csharp
// a)
int j = 1; 
int i = 1;
bool b = !(j == 3) || ( i > j && j <= i);

// b)
bool b = true || false;

// c)
bool b = 1 == 1 && 10 == 10 || 100 == 100;

// d) 
bool x = true; 
bool b = !x; 
b = !b && b;

// e)
bool x = false; 
bool b = false; 
if (x && b)
{
    b = !x || x;
}
```
{% endtab %}

{% tab title="Lösung" %}
Was ist jeweils der Wert der Variable `b`  nach Durchlauf des Code-Abschnittes?  

```csharp
// a)
int j = 1; 
int i = 1;
bool b = !(j == 3) || ( i > j && j <= i);      // b = true

// b)
bool b = true || false;                        // b = true

// c)
bool b = 1 == 1 && 10 == 10 || 100 == 100;     // b = true

// d) 
bool x = true; 
bool b = !x; 
b = !b && b;                                   // b = false

// e)
bool x = false; 
bool b = false; 
if (x && b)
{
    b = !x || x;
}                                              // b = false
```
{% endtab %}
{% endtabs %}

### Aufgabe 7

{% tabs %}
{% tab title="Aufgabe" %}
Was sind die Werte im `a` Array nach Durchlauf des Code-Abschnittes?  

```csharp
int[] a = new int[4];

for (int i = 0; i < a.Length - 1; i++)
{
    if (i == 1)
    {
        a[i] = 3;
    }
    if (i == 2)
    {
        a[i] = 2;
    }
    if (i == 3)
    {
        a[i] = 1;
    }
    if (i == 4)
    {
        a[i] = i;
    } 
}
```
{% endtab %}

{% tab title="Lösung" %}
Was sind die Werte im `a` Array nach Durchlauf des Code-Abschnittes?  

```csharp
int[] a = new int[4];

for (int i = 0; i < a.Length - 1; i++)
{
    if (i == 1)
    {
        a[i] = 3;
    }
    if (i == 2)
    {
        a[i] = 2;
    }
    if (i == 3)
    {
        a[i] = 1;
    }
    if (i == 4)
    {
        a[i] = i;
    } 
}
```

#### Lösung

```csharp
a[0] = 0
a[1] = 3 
a[2] = 2
a[3] = 0
```
{% endtab %}
{% endtabs %}

### Aufgabe 8

{% tabs %}
{% tab title="Aufgabe" %}
Was sind die Werte im `a` Array nach Durchlauf des Code-Abschnittes?  

```csharp
string[] a = new string[3];
int b = 10;

for (int i = 0; i < a.Length; i++) {
    a[i] = (b / 2);
    b *= 2;
}
```
{% endtab %}

{% tab title="Lösung" %}
Was sind die Werte im `a` Array nach Durchlauf des Code-Abschnittes?  

```csharp
string[] a = new string[3];
int b = 10;

for (int i = 0; i < a.Length; i++) {
    a[i] = (b / 2);
    b *= 2;
}
```

#### Lösung

{% hint style="danger" %}
Kein Resultat -&gt; **Cannot implicitly convert type int to string**
{% endhint %}
{% endtab %}
{% endtabs %}

### Aufgabe 9

{% tabs %}
{% tab title="Aufgabe" %}
Was ist der Wert der Variable `j`  nach Durchlauf des Code-Abschnittes?  

```csharp
List<string> list = new List<string>();

int j = 10; 
list.Add("Hallo Welt");

for (int i = 0; i < list.Count; i++)
{
    list.Add(i.ToString());
}

j = Convert.ToInt32(list[1]);
```
{% endtab %}

{% tab title="Lösung" %}
Was ist der Wert der Variable `j`  nach Durchlauf des Code-Abschnittes?  

```csharp
List<string> list = new List<string>();

int j = 10; 
list.Add("Hallo Welt");

for (int i = 0; i < list.Count; i++)
{
    list.Add(i.ToString());
}

j = Convert.ToInt32(list[1]);
```

#### Lösung

{% hint style="danger" %}
Kein Resultat -&gt; **Endlosschleife**
{% endhint %}
{% endtab %}
{% endtabs %}

### Aufgabe 10

{% tabs %}
{% tab title="Aufgabe" %}
Folgende Variablen seien definiert:

```csharp
int[,] a = new int[2, 5]; 
int[] c = { 1, 2, 3, 4 }; 
int i = 10;
```

Betrachten Sie die folgenden Anweisungen und entscheiden Sie, welche korrekt und welche falsch sind. Fehlerhafte Programmzeilen sind durchzustreichen. Begründen Sie, wieso eine Anweisung falsch ist, z.B. nicht kompatibler Typ. Korrekte Programmzeilen müssen Sie mit einem OK bezeichnen.

```csharp
a[0, 0] = i; 
a[1, 5] = c[0]; 
a[0, 1] = 15; 
i = a[0, 1]; 
a[1, 1] = 8;
```
{% endtab %}

{% tab title="Lösung" %}
Folgende Variablen seien definiert:

```csharp
int[,] a = new int[2, 5]; 
int[] c = { 1, 2, 3, 4 }; 
int i = 10;
```

Betrachten Sie die folgenden Anweisungen und entscheiden Sie, welche korrekt und welche falsch sind. Fehlerhafte Programmzeilen sind durchzustreichen. Begründen Sie, wieso eine Anweisung falsch ist, z.B. nicht kompatibler Typ. Korrekte Programmzeilen müssen Sie mit einem OK bezeichnen.

#### Lösung

![](../.gitbook/assets/image%20%28163%29.png)
{% endtab %}
{% endtabs %}

### Aufgabe 11

{% tabs %}
{% tab title="Aufgabe" %}
Folgende Klassen, Variablen und Zuweisungen seien definiert:

```csharp
public class Baum
{
    int _hoehe, _breite;
    
    public Baum(int hoehe, int breite)
    {
        _hoehe = hoehe;
        _breite = breite; 
    }
    public int Hoehe
    {
        get { return _hoehe; }
    }
    public int Breite
    {
        get { return _breite; }
    }
}

public class Punkt
{
    int _x, _y;
    public Punkt(int x, int y)
    {
        _x = x;
        _y = y;
    }
    public int X
    {
        get { return _x; }
        set { _x = value; }
    }
    public int Y
    {
        get { return _y; }
        set { _y = value; }
    }
}

string s = "abcd";
int[] a1 = { 1, 2, 3, 4 };
byte b = 56;
Punkt p = new Punkt(a1[0], 100); 
Baum[] ba = new Baum[3];
Baum baum = new Baum(80, 2);
```

Betrachten Sie nun die folgenden Anweisungen und entscheiden Sie, welche korrekt sind und welche falsch sind. Fehlerhafte Programmzeilen sind durchzustreichen. Begründen Sie, wieso eine Anweisung falsch ist, z.B. nicht kompatibler Typ. Korrekte Programmzeilen bezeichnen Sie mit einem OK.

```csharp
a1[0] = b;
a1[4] = p.X;
ba[1] = new Baum(2, 3); 
ba[2] = baum;
Baum neuerBaum = ba[0]; 
baum = p;
a1[0] = baum.Hoehe; 
p.Y = baum.Hoehe; 
baum.Breite = 0;
b = (byte)ba[0].Breite; 
ba = null;
p.X = s.Length;
```
{% endtab %}

{% tab title="Lösung" %}
Folgende Klassen, Variablen und Zuweisungen seien definiert:

```csharp
public class Baum
{
    int _hoehe, _breite;
    
    public Baum(int hoehe, int breite)
    {
        _hoehe = hoehe;
        _breite = breite; 
    }
    public int Hoehe
    {
        get { return _hoehe; }
    }
    public int Breite
    {
        get { return _breite; }
    }
}

public class Punkt
{
    int _x, _y;
    public Punkt(int x, int y)
    {
        _x = x;
        _y = y;
    }
    public int X
    {
        get { return _x; }
        set { _x = value; }
    }
    public int Y
    {
        get { return _y; }
        set { _y = value; }
    }
}

string s = "abcd";
int[] a1 = { 1, 2, 3, 4 };
byte b = 56;
Punkt p = new Punkt(a1[0], 100); 
Baum[] ba = new Baum[3];
Baum baum = new Baum(80, 2);
```

Betrachten Sie nun die folgenden Anweisungen und entscheiden Sie, welche korrekt sind und welche falsch sind. Fehlerhafte Programmzeilen sind durchzustreichen. Begründen Sie, wieso eine Anweisung falsch ist, z.B. nicht kompatibler Typ. Korrekte Programmzeilen bezeichnen Sie mit einem OK.

#### Lösung

![](../.gitbook/assets/image%20%2817%29.png)
{% endtab %}
{% endtabs %}

