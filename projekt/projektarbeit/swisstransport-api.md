# SwissTransport API

Im Projekt SwissTransport, das bereits in eurer Solution vorhanden ist, befindet sich Code, der es euch erlaubt, auf die SwissTransport API zuzugreifen.

![Klassendiagramm SwissTransport](../../.gitbook/assets/image%20%28160%29.png)

Eine \(optionale\) [Anforderung](./#anforderungen) erfordert es, dass eine zusätzliche Methode in `Transport` programmiert wird, welche zusätzlich Datum und Uhrzeit entgegennimmt.

Dafür wird sicher die [API Dokumentation](https://transport.opendata.ch/) hilfreich sein.

## Die Transport API verwenden

Um die Transport API zu verwenden, musst du in deiner Klasse eine Instanz der `Transport` Klasse erstellen.

```csharp
ITransport transport = new Transport();
```

