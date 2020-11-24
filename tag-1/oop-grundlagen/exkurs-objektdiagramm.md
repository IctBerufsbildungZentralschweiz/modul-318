# 📖💡 Exkurs: Objektdiagramm

## Das Objektdiagramm

Ein Objektdiagramm ist im Gegensatz zum Klassendiagramm eine Momentaufnahme eines Programms. Auch für das Objektdiagramm gibt es einen UML Standard. Nachfolgend seht ihr ein Objektdiagramm mit einem einzelnen Objekt.

![](../../.gitbook/assets/image%20%28144%29.png)

Quelle: [http://mbse.se-rwth.de/book1/index.php?c=chapter4-1](http://mbse.se-rwth.de/book1/index.php?c=chapter4-1)

## Beispiel

In diesem Beispiel gehen wir das Beispiel aus [Aufgabe 11 der Übung C\# Grundlagen](../uebung-c-grundlagen.md#aufgabe-11) durch und zeichnen Schritt für Schritt ein Objektdiagramm. Wichtig dabei, das Objektdiagramm ist immer eine **Momentaufnahme**, es ändert sich also nach jeder Zeile Code, die ausgeführt wurde.

Gegeben sind folgende Klassen:

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
```

### Ausgangslage

{% tabs %}
{% tab title="Ausgangslage" %}
```csharp
string s = "abcd";
int[] a1 = { 1, 2, 3, 4 };
byte b = 56;
Punkt p = new Punkt(a1[0], 100); 
Baum[] ba = new Baum[3];
Baum baum = new Baum(80, 2);
```

![](../../.gitbook/assets/image%20%2810%29.png)
{% endtab %}

{% tab title="Schritt für Schritt" %}
### Ausgangslage 1. Schritt

```csharp
string s = "abcd";
```

![](../../.gitbook/assets/image%20%2872%29.png)

### Ausgangslage 2. Schritt

```csharp
int[] a1 = { 1, 2, 3, 4 };
```

![](../../.gitbook/assets/image%20%2814%29.png)

### Ausgangslage 3. Schritt

```csharp
byte b = 56;
```

![](../../.gitbook/assets/image%20%2886%29.png)

### Ausgangslage 4. Schritt

```csharp
Punkt p = new Punkt(a1[0], 100); 
```

![](../../.gitbook/assets/image%20%2828%29.png)

### Ausgangslage 5. Schritt

```csharp
Baum[] ba = new Baum[3];
```

![](../../.gitbook/assets/image%20%2842%29.png)

### Ausgangslage 6. Schritt

```csharp
Baum baum = new Baum(80, 2);
```

![](../../.gitbook/assets/image%20%2883%29.png)
{% endtab %}
{% endtabs %}

### 

### 1. Schritt

```csharp
a1[0] = b;
```

![](../../.gitbook/assets/image%20%2815%29.png)

### 2. Schritt

```csharp
ba[1] = new Baum(2, 3); 
```

![](../../.gitbook/assets/image%20%2882%29.png)

### 3. Schritt

```csharp
ba[2] = baum;
```

![](../../.gitbook/assets/image%20%2823%29.png)

{% hint style="warning" %}
Beachte, dass das Objekt **nicht kopiert** wird. Es gibt jetzt lediglich eine zweite Referenz auf dieses Objekt. Es existiert aber nur einmal im Speicher.
{% endhint %}

### 4. Schritt

```csharp
Baum neuerBaum = ba[0];
```

![](../../.gitbook/assets/image%20%28158%29.png)

### 5. Schritt

```csharp
a1[0] = baum.Hoehe;
```

![](../../.gitbook/assets/image%20%2890%29.png)

### 6. Schritt

```csharp
p.Y = baum.Hoehe;
```

![](../../.gitbook/assets/image%20%28143%29.png)

### 7. Schritt

```csharp
ba = null;
```

![](../../.gitbook/assets/image%20%28145%29.png)

{% hint style="info" %}
Da es keine Referenz mehr auf das Baum Array gibt, wird dies irgendwann vom Garbage Collector abgeräumt und aus dem Speicher gelöscht. Dasselbe passiert dann mit dem Objekt unten rechts, da es keine Referenz mehr darauf gibt.
{% endhint %}

### 8. Schritt

```csharp
p.X = s.Length;
```

![](../../.gitbook/assets/image%20%2871%29.png)

So ergibt sich schlussendlich dieses Objektdiagramm:

![](../../.gitbook/assets/image%20%2826%29.png)



## 💡 Aufgabe

Zeichne das Objektdiagramm auf Papier nach der Ausführung des folgenden Codes:

```csharp
ba = new Baum[] { neuerBaum, baum, new Baum(50, 8) };
```



