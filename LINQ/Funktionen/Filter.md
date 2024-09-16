## Filter

- um Werte zu erhalten diese auf bestimmte Kriterien zutreffen

### Verwendung:

- verwendung der Filter ist wie bei einer `if`-Abfrage

**Beispiel Abfragen**
- `.Compare()`  
- `.Contains()`  
- `.Equals()`  
- `x >= y`  
- `!boolVar`  

&nbsp;

### Beispiele:

Code:
```cs
string[] names = { "Uwe", "Daniel", "Julian", "Chris" };

//QUERY SYNTAX
var linq = from name in names
           where name.Contains('e')
           select name;

//METHOD SYNTAX
var linq = names.Where(name => name.Contains('e'));

foreach (string name in linq) 
{
    Console.WriteLine(name);
}
```

Output:
```
Uwe
Daniel
```

&nbsp;
---
&nbsp;

```cs
namespace Program
{
    class Program
    {
        static void Main() 
        {
            List<Tier> tiere = new List<Tier>();
            tiere.Add(new Hund("Bello", 2));
            tiere.Add(new Katze("Katzi", 5));

            //QUERY SYNTAX
            var hunde = from hund in tiere.OfType<Hund>() select hund;
            
            //METHOD SYNTAX
            var hunde = tiere.Select(hund => hund).OfType<Hund>().ToList();

            foreach (var hund in hunde) 
            {
                Console.WriteLine("Ein Hund heißt " + hund.Name + "!");
            }
        }
    }
    
    class Tier 
    {
        public string Name { get; set; }
        public int Age { get; set; }
    }
    
    class Hund : Tier
    {
        public Hund(string name, int age) 
        {
            Name = name;
            Age = age;
        }
    }

    class Katze : Tier
    {
        public Katze(string name, int age)
        {
            Name = name;
            Age = age;
        }
    }
}
```

Output:
```
Ein Hund heißt Bello!
```