## Mathematic

### Verwendung:

**METHODS**
- `Max`
- `Min`
- `Average`
- `Sum`
- `Count`
- `Aggregate((EXPRESSION, EXPRESSION) => EXPRESSION OPERATION EXPRESSION)`

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