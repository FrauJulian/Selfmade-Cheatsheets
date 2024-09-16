## Method Syntax

- C# Code
- bei wenigen Anwendungsfällen pflicht

### Aufbau:

```cs
DATA.METHOD(EXPRESSION OPTIONS).OPTIONS(EXPRESSION OPTIONS);
```

- `DATA` > Daten z.B. Listen, Arrays
- `METHOD` > LINQ Methode
- `EXPRESSION` > expression
- `OPTIONS` > optionale LINQ Methoden

&nbsp;

### Beispiel:

Code:
```cs
string[] names = { "Uwe", "Daniel", "Julian", "Chris" };

var linq = names.Select(name => name);

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