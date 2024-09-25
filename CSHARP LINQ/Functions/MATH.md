## Mathematic

### Verwendung:

**METHODS**
- `Max` - Maximaler Wert
- `Min` - Minimaler Wert
- `Average` - Durchschnittlicher Wert
- `Sum` - Summe aller Zahlen
- `Count` - Anzahl der Zahlen
- `Aggregate()` - sonder Operationen ausführen

&nbsp;

### Beispiel:

Code:
```cs
int[] numbers = new int[] { 5, 6, 8, 14, 1, 3, 18 };

//METHOD SYNTAX
var result = numbers.Average();

//QUERY SYNTAX
var result = (from number in numbers 
              select number).Average();

Console.WriteLine(result);
```

Output:
```
7,857142857142857
```