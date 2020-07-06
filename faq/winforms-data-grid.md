# ❓ WinForms DataGridView

## Spalten

![Spalten bearbeiten](../.gitbook/assets/grafik%20%281%29.png)

![Spalte hinzuf&#xFC;gen](../.gitbook/assets/grafik%20%284%29.png)

![Spalte konfigurieren](../.gitbook/assets/grafik%20%2821%29.png)

## Reihen

Es gibt verschiedene Arten, wie Reihen dem Grid hinzugefügt werden können. Hier werden zwei Varianten gezeigt.

### Rows und ein String-Array

```csharp
balanceChangesGrid.Rows.Add(new[]
{
    "15:00:00",
    "1.00",
    "20.00"
});
```

Dies ist die simpelste Variante. Pro Reihe wird ein String-Array dem Rows-Liste auf der DataGridView hinzugefügt. Diese werden in der Reihenfolge des Arrays in den jeweiligen Spalten angezeigt. Falls die Reihenfolge der Spalten sich ändert muss man das beachten.

{% hint style="info" %}
Diese Variante wurde in der Musterlösung der Aufgabensammlung Nr 4.2 und 4.3 verwendet
{% endhint %}

### DataSource und eine Liste mit Objekten

![Konfiguration einer Spalte f&#xFC;r eine DataSource, inkl. Format](../.gitbook/assets/grafik%20%2814%29.png)

```csharp
// Member-Variable mit Binding List
private BindingList<BalanceChangelogEntry> balanceChangelogEntries = new BindingList<BalanceChangelogEntry>();

// Im FormLoad
balanceChangesGrid.DataSource = balanceChangelogEntries;

// Beim Hinzüfugen der Reihe
balanceChangelogEntries.Add(new BalanceChangelogEntry
{
    BalanceChange = 1,
    NewBalance = 20,
    Time = DateTime.Now
});
```

Für eine Liste mit Objekten eignet sich die leicht kompliziertere Variante der BindingList und DataSource. Nachdem die DataSource zugewiesen wurde können die Reihen des Grids durch die Liste verwaltet werden.

{% hint style="info" %}
Diese Variante wurde in der Musterlösung der Aufgabensammlung Nr 4.4 verwendet
{% endhint %}

