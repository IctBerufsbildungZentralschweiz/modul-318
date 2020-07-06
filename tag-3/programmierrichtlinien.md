# 📖💡 Coderichtlinien

## Was sind Coderichtlinien?

> "Ein Programmierstil \(engl. code conventions, coding conventions, coding standards\) ist in der Programmierung das Erstellen von Quellcode nach bestimmten vorgegebenen Regeln. Er gilt als Teilaspekt von Softwarequalität, der insbesondere die Verständlichkeit und Wartbarkeit von Software, dies sind Kriterien für Softwarequalität gem. ISO/IEC 9126 \(aktualisiert durch ISO/IEC 25000\) unterstützen soll." - Wikipedia 2020

In einem Team muss man sich auf einen bestimmten Programmierstil einigen, damit der ganze Source Code einigermassen einheitlich daher kommt und man sich gut zurechtfindet. Oft wird das über Coderichtlinien gelöst. Es gibt z.B. firmenweite Coderichtlinien für eine Sprache, oder im Fall von C\# gibt es sogar von Microsoft selbst empfohlene Richtlinien, an welche sich immer mehr Teams versuchen zu halten.



## C\# Coding Guidelines von Microsoft

Hier findet ihr die kompletten Coding Guidelines von Microsoft:

[https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)

## ReSharper / StyleCop

![](../.gitbook/assets/image%20%2867%29.png)

Heute gibt es Tools, die es einem erleichtern, Code zu schreiben, der sich an Coderichtlinien hält. Mit ReSharper und StyleCop lässt sich der Code analysieren und teilweise sogar automatisch korrigieren, sodass er den Richtlinien entspricht, gut eingerückt ist, keine ungebrauchten Usings hat usw. 

Hier findet ihr weitere infos zu Resharper:  
[https://www.jetbrains.com/resharper/](https://www.jetbrains.com/resharper/)

Hier zu StyleCop:  
[https://blog.submain.com/stylecop-detailed-guide/](https://blog.submain.com/stylecop-detailed-guide/)



## 💡 Aufgabe: schlechte Codebeispiele verbessern

Nachfolgend findest du einige Codeschnipsel, welche sich nicht an die Richtlinien halten. Bestimme, was nicht gut ist und wie man es besser machen könnte.

### Aufgabe 1

```csharp
public class Person
{
private Point _position;
public void Walk()
{
this._position.x += 10;
}
}
```

### Aufgabe 2

```csharp
public class Person
{
    public Person[] _children;
    public string Name { get; set; }
    
    public void SayChildrensNames() {
        foreach (Person child in this._children) {
            Console.WriteLine(child.Name);
        }
    }
}
```

### Aufgabe 3

```csharp
public class person
{
    private string name { get; private set; }
    
    public string rename(string newname)
    {
        this.name = newname;
    }
}
```

### Aufgabe 4

```csharp
public static class Program
{
    public static void Main() 
    {
        var a = new Person();
        var b = new Car();
        
        b.Owner = a;
        
        var c = b.Breaks;
        var d = c.Material;
        
        Console.WriteLine($"{a.Name} drives a {b.Brand} with {c.Name} breaks made of {d}");
    }
}
```

### Aufgabe 5

```csharp
public static class Program
{
    public static void Main() 
    {
        var person=new Person();
        var children=person.Children;
        for(i=0;i<children.Count;i++){
            children[i].Walk();
        }
    }
}
```

