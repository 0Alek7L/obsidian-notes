#Fundamentals 
list.Sort();
list = list.OrderBy(num => num).ToList();   /lower to higher
list = list.OrderByDescending(num => num).ToList();   //higher to lower

class Student
{
	public int age;
	public string name;
}
List<\Student> students = new List<\Student>();
Student dimitrichko = new Student();
	dimitrichko.age = 18;
	dimitrichko.name = "Dimitrichko";
students = students.OrderBy(s=>s.name).ThenBy(s=>s.age);