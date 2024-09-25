## Gruppierung

- um Elemente in bestimmte Gruppen unterzuordnen

### Verwendung:

**QUERY OPTIONS**
- `group x by y`

**METHOD**
- `GroupBy`

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
            menschen.Add(new Person("Chris", "Hausner", "Programmierer"));
            menschen.Add(new Person("Damian", "Kellner", "Bäcker"));
            menschen.Add(new Person("Anton", "Kapler", "Bäcker"));
            menschen.Add(new Person("Roman", "Kowalski", "Programmierer"));
            menschen.Add(new Person("Anton", "Hundler", "Bäcker"));

            //QUERY SYNTAX
            var groups = from person in menschen
                         group person by person.Job;

            //METHOD SYNTAX
            var groups = menschen.GroupBy(person => person.Job);

            foreach (var group in groups) 
            {
                Console.WriteLine(group.Key);
            }
        }
    }
    
    class Person 
    {
        public string Firstname { get; set; }
        public string Lastname { get; set; }
        public string Job { get; set; }

        public Person(string firstName, string lastName, string job) 
        {
            Firstname = firstName;
            Lastname = lastName;
            Job = job;
        }
    }
}
```

Output:
```
Programmierer
Bäcker
```