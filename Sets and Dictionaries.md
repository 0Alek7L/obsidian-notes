#Advanced 
   **DICTIONARIES**

	1.Dictionary<K, V> Overview
	2.Multi-Dictionaries
	A key holds multiple values
	3.Nested Dictionaries
	A dictionary holding another dictionary

Dictionary<int, string> studentAges = new Dictionary<int, string>();       //normal dictionary

SortedDictionary<int, string> studentAges = new SortedDictionary<int, string>;       //sorted dictionary

	studentAges.Add(1, "1");
	studentAges.Add(5, "5");
	studentAges.Add(12 "2")
	studentAges.Add(13, "13");

SortedDictionary<DateTime, string> events = new SortedDictionary<DateTime, string>();

	events.Add(new DateTime (2022, 5, 18), "Top Event");
	events.Add(new DateTime (2022, 5, 2), "Football");
	events.Add(new DateTime (2022, 5, 5), "Tennis");
	events.Add(new DateTime (2022, 5, 9), "Skuka");
	events.Add(new DateTime (2022, 5, 23), "Nehsto");
	//output: 02/05/2022 12:00:00 am - Football... (!!SORTED!!)

foreach(var item in studentAges){
	Console.WriteLine($"{item.Key} - {item.Value}");
}   // цикъл за обхождане

ContainsKey(key) - fast!
ContainsValue(value) - slow! Never use it!

studentGrades = studentGrades.OrderBy(x => x.Value)
	.ThenBy(x => x.Key, x => x.Value)
	.ToDictionary(x => x.Key, x => x.Value);

ВСЯКА ЗАДАЧА, КОЯТО МОЖЕ ДА СЕ РЕШИ С РЕЧНИК МОЖЕ ДА СЕ РЕШИ С ОБЕКТИ! 

    public class Cloth
    {
    public sting Name {get; set;}
    public string Color {get; set;}
    public int Count {get; set;}
    }

---
   **SETS**

Set<\T>

	A set keeps unique elements
	Allows *add*/*remove*/*search* elements
	Very fast performance 
HashSet<\T>

	Keeps a set of elements in a hash-table
	Elements are in no particular order
	Similar to List<\T>, but more efficient 
		Example:
		HashSet<\string> set = new HashSet<\string>();
			set.Add("Peter");
			set.Add("Peter");//Existing element -> not added again
			set.Add("George");
		Console.WriteLine(string.Join(" ", set));       //Peter, George
		Console.WriteLine(set.Contains("Maria"));  //False
		Console.WriteLine(set.Contains("Peter"));  //True

---
List<\T>
	- Fast "*add*"
	- Slow "*search*" and "*remove*"
HashSet<\T>
	- Fast "*add*", "*search*" and "*remove*"
 
[[Streams, Files and dictionaries]]