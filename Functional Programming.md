#Advanced 

List<\int> list = new List<\int> {1,2,3,4,5,6,7,8,9,10};

**DECLARATIVE**

    int sum = list.Where(x=>x%2==0).Sum();

**IMPERATIVE**

    List<int> evenNumbets = new List<int>();
    for(int i=0; i<list.Count; i++){
        if(list[i]%2==0)
            evenNumbers.Add(list[i]);
    }....
----
**Lambda Expressions**

	(parameters)=>{body}
	Implicit lambda expression
	-msg=>Console.WriteLine(msg);
	- Explicit lambda expression
	-(String msg)=>{Console.WriteLine(msg);}
	- Zero parameters
	-()=>{Console.WriteLine("hi");}
	- Multiple parameters 
	-(int x, int y)=>{return x+y;}

	int[] evenNums = array.Where(number=>{
	Console.WriteLine($"{number} % 2 = {number%2}");
	return number%2==0;
	}).ToArray();

---
 **Func<\T>** **Functions**

	Func<(input t), (output t)> name = lambda expression;
	Func<int, string> func = n=>n.ToString();

**Action<\T>**

	This is a void method
	Action<string> print = message=>Console.WriteLine(message);
	print("text");//calls the void method

**Delegate**

	delegate int TwoNumbersOperation(decimal a, float b);(outside of the method)
	TwoNumbersOperation(decimal delegateFunc = Sum;(inside main)
	(sum is a method that sums a & b)
	Console.WriteLine(delegateFunc(5, 6));

**Predicate**

	This is a method which returns boolean
	Predicate<int> predicate = FilterEven;//use lambda in predicates
	-----------
	List<Predicate<int>> predicates = new();
	predicates.Add(n => n % divider == 0);

---
**DIFFICULT TASK** https://pastebin.com/yLZLafV4

	Action<string> print = strings=> Console.WriteLine(string. Join(Environment.NewLine, strings));
	string[] strings = Console.ReadLine().Split("",
	StringSplitOptions.RemoveEmptyEntries); print(strings);
	//This reads an array and prints each item on new line

---
**IMPLEMENTATION IN PROPERTY (goes to) 
	-> https://prnt.sc/-BS_wmGIReNQ
	-> https://prnt.sc/atAN_H_UB85S
