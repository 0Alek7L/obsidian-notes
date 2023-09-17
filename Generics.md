#Advanced 

	void Print<T>(T a)
        {
            T anyTypeVariable = default(T);
            Console.WriteLine(a);
        }
	------------------------------
	        Print<int>(5);
            Print<float>(5.12f);
            Print<string>("yes");
            Print<char>('a');

---

	PrintHuman<Stident>() {new Student() {Name="Pesho"}};//Pesho
	void PrintHuman<T>(T human) where T : Human
	{
		Console.WriteLine(human.Name);
	}
	class Human
	{
		public string Name {get;set;}
	}
	class Student: Human
	{
		public int Score {get; set;}
	}

----