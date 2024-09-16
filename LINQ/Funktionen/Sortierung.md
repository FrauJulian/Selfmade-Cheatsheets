## Sortierung

- um Werte Alphabetisch zu sortieren

### Verwendung:

**QUERY OPTIONS**
- `ascending` (Alphabetisch Absteigend | a > z) - DEFAULT
- `descending` (Alphabetisch Aufsteigend | z > a)

**METHODS**
- `OrderByAscending` (Alphabetisch Absteigend | a > z) - DEFAULT
- `OrderByDescending` (Alphabetisch Aufsteigend | z > a)

&nbsp;

### Beispiel:

Code:
```cs
namespace Program
{
    class Program
    {
        static void Main() 
        {
            List<Person> menschen = new List<Person>();
            menschen.Add(new Person("Chris", "Hausner"));
            menschen.Add(new Person("Damian", "Kellner"));
            menschen.Add(new Person("Anton", "Kapler"));
            menschen.Add(new Person("Roman", "Kowalski"));
            menschen.Add(new Person("Anton", "Hundler"));
            
            //QUERY SYNTAX
            var personen = from person in menschen 
                           orderby person.Firstname /*OPTIONS*/, person.Lastname /*OPTIONS*/
                           select person;

            //METHOD SYNTAX
            var personen = menschen.OrderBy(person => person.Firstname).ThenBy(person => person.Lastname);

            foreach (var person in personen) 
            {
                Console.WriteLine("Eine Person heißt " + person.Firstname + " " + person.Lastname + "!");
            }
        }
    }
    
    class Person 
    {
        public string Firstname { get; set; }
        public string Lastname { get; set; }

        public Person(string firstName, string lastName) 
        {
            Firstname = firstName;
            Lastname = lastName;
        }
    }
}
```

Output:
```
Eine Person heißt Anton Hundler!
Eine Person heißt Anton Kapler!
Eine Person heißt Chris Hausner!
Eine Person heißt Damian Kellner!
Eine Person heißt Roman Kowalski!
```