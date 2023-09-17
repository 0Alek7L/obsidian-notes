#OOP  ==ИЗГЛЕДАЙ ЛЕКЦИИТЕ ОТНОВО==
ПРЕПОРЪЧИТЕЛНО Е ДА СЕ ИЗБЯГВА REFLECTION
							==БАВЕН E==

=>Код за автоматично преброяване на класове 
	-> https://prnt.sc/qRQKzyj4ij8t

---
```
Type listType = typeOf(List<int>);
Type[] interfaces = listType.GetInterfaces();
foreach(Type interface in interfaces)
{
	Console.WriteLine(interface.Name);
}
```
---
```
Type type = typeOf(Robot);
Robot robot = (Robot)Activator.CreateInstance(type);
//създаваме инстанция на Robot, но кастваме, защото връща обект
//Еквивалент на = new Robot();
class Robot{} //има конструктор
```
---
```
Type type = typeOf(Car);//car has many fields
{1} FieldInfo[] fields = type.GetFields(BindingFlags.Instance | BindingFlags.Static | BindingFlags.NonPublic | BindingFlags.Public); 
//BindingFlags->built-in enum
//Operator "|" means "OR"
{2} FieldInfo[] fields = type.GetFields((BindingFlags)60); 
//absolutely the same as {1}
foreach(FieldInfo field in fields)
{
	Console.WriteLine(field.Name);
}
```
---