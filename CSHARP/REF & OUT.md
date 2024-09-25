## Ref & Out

### Ref:

Wenn ein Parameter in einer Method geändert wird ist dieser außerhalb der Methode gleich.

**Verwendung:**

Verwende `ref`, wenn der Parameter vorher einen Wert haben muss.

**Beispiel:**

Code:
```cs
int numberRef = 1;
Console.WriteLine(numberRef);
ExampleRef(ref numberRef);
Console.WriteLine(numberRef);

void ExampleRef(ref int number)
{
    number = 3;
}
```

Output:
```
1
3
```

&nbsp;

### Out:

Parameter darf nicht initialisiert sein. Wenn Parameter innerhalb der Method gesetzt wird ist dieser außerhalb identisch.

**Verwendung:**

Verwende `out`, wenn der Parameter von der Methode initialisiert wird und kein vorheriger Wert benötigt wird.

**Beispiel:**

```cs
int numberOut;
ExampleOut(out numberOut);
Console.WriteLine(numberOut);

void ExampleOut(out int number)
{
    number = 6;
}
```

Output:
```
6
```