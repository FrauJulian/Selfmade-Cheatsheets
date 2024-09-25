## Query Syntax

- ähnelt dem SQL Syntax
- bessere lesbarkeit

### Aufbau:

```cs
from EXPRESSION_NAME in DATA OPTIONS select EXPRESSION_NAME;
```

- `DATA` > Daten z.B. Listen, Arrays
- `OPTIONS` > optionale LINQ Methoden
- `EXPRESSION_NAME` > Name der expression

&nbsp;

### Beispiel:

Code:
```cs
string[] names = { "Uwe", "Daniel", "Julian", "Chris" };

var linq = from name in names select name;

foreach (string name in linq) 
{
    Console.WriteLine(name);
}
```

Output:
```
Uwe
Daniel
Julian
Chris
```