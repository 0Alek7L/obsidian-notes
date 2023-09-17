#Advanced
- Property - Capital letter
- Field - normal letter
- this - refers to the variable in the same class
- use propfull to create a property and a field
- ude ctor to create a constructor 
Example:

	class Student
	{
		private string firstName;
		private string LastName;
		public string FirstName
		{
			get { return firstName; }
			set { firstName = value;}
		}
		public string LastName
		{
			get { return lastName; }
			set { lastName = value;}
		}
		----------------------------
		public sting FullName{
		get {return $"{this.firstName} {this.LastName}"}
		}
	}

Constructors example:

	public class Car
	{
		public Car(string make, string model, int year)
		{
			Make = make;
			Model = model; 
			Year - year;
		}
		public Car (string make, string model, int year, double fuelquantity, double fuelConsumption) : this (make, model, year) 
		{
			FuelQuantity = fuelQuantity:
			FuelConsumption = fuelConsumption;
		}
	}

**ENUMERATIONS**
We can name many things and give them numbers

	namespace DirectionsEnum{
		public enum Direction
		{
			left=0,
			right=1,
			up=2,
			down=3,
		}
	}
	(In another class)
	using DirectionsEnum;
	{
		public void Main(...)
		{
			Console.WriteLine((int)Direction.down);//3
			Console.WriteLine((Direction)3);//down 
			-------------------------------------
			Direction dir = (Direction)0;//left
		}
	}

Обхождане

	foreach(var item in Enum.GetValues(typeof(Direction)))
	{
		Console.WriteLine(item);
	}

**Static Class**
- a static class is declared by the *static* keyword 
- It cannot be instantiated 
- You cannot declare variables from its type
- You access its members by using its name
- like Math.Round(num)


**If a class is static all methods in it are static.** 
For example if it is static **or non-static but with static method**:
	Printer.Print();
If it isn't:
	new Printer().Print();