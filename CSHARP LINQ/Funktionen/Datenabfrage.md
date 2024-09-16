## Datenabfrage

### Verwendung:

**METHODS**  
- `LastOrDefault` - letztes Element ansont Standartwert
- `Last` - letztes Element ansont Ausnahme
- `FirstOrDefault` - erstes Element ansont Standartwert
- `First` - erstes Element ansont Ausnahme
- `SingleOrDefault` - einzelnes Element, wenn ein Wert vorhanden ist ansont Standartwert/Ausnahme **********
- `Single` - einzelnes Element, wenn ein Wert vorhanden ist ansont Ausnahme

&nbsp;

### Beispiel:

Code:
```cs
string[] names = { "Uwe", "Daniel", "Julian", "Chris" };

var linq = names.First();

Console.WriteLine(linq);
```

Output:
```
Uwe
```