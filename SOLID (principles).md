#OOP 

**S  -> Single Responsibility
O -> Open/Closed
L  -> Liskov substitution
I   -> Interface Segregation
D -> Dependency Inversion**

---
ОБЯСНЕНИЕ В ЕДНО ИЗРЕЧЕНИЕ
--
1. Single Responsibility Principle (SRP): A class should have only one reason to change, meaning it should have only one responsibility or concern.
2. Open/Closed Principle (OCP): Software entities (classes, modules, etc.) should be open for extension but closed for modification, allowing for easy addition of new functionality without changing existing code.
3. Liskov Substitution Principle (LSP): Objects of a base class should be replaceable with objects of a derived class without affecting the correctness of the program.
4. Interface Segregation Principle (ISP): A client should not be forced to depend on interfaces it does not use, promoting smaller, more focused interfaces.
5. Dependency Inversion Principle (DIP): High-level modules should not depend on low-level modules, but both should depend on abstractions (interfaces or abstract classes).
---
==Single Responsibility== (SRP)
--
->**Every class should be responsible for only a *single part of the functionality* and that responsibility should be entirely *encapsulated* by the class.

---
==Open/Closed Principle== (OCP)
--
->Software entities like classes, modules and functions should be **open for extension, but closed for modifications**
->**Extensibility**
	Adding a new behavior **doesn't require** changes over existing source code 
->**Reusability**
	Subsystems are **suitable for reusing** in other projects - modularity

---

==Liskov Substitution== (LSP)
--
**CHILD CLASS MUST NOT VIOLATE BASE CLASS BEHAVIOR**
->Derived class must be completely substitutable for their base types
->Parent class трябва да бъде лесно заменим с неговия sub class
	-Derived classes:
		only **extend** functionalities of the base class
		must **not** remove base class behavior

**APPROACHES**
->Tell Don't Ask
	If you need to check what is the object - move the behavior **inside the object**
->There shouldn't be any **virtual** methods in **constructors**
->New Base Class
	If 2 classes share common behavior, but are not substitutable, create a third from which both derive:
```
		C <- third class
	   / \
      /   \
    A   ~   B <- two classes that share common behavior
```

---

==Interface Segregation== (ISP)
--
**FAT INTERFACE -> SMALL INTERFACE**
->Segregate Interfaces
	>Prefer **small, cohesive** (lean and focused) interfaces
	>Divide "**fat**" interfaces into "**role**" interfaces 
\*Classes whose interfaces are not cohesive have "fat" interfaces
->The "fat" interfaces implement **a number of small** interfaces with just what you need
->All **public members** of a class divided in separate classes - again, could be thought of as an interface

---

==Dependency Inversion== (DIP)
--
A dependency is any component/system-> https://prnt.sc/pr-akqSsFWri
->depend on abstractions -> https://prnt.sc/j-oOtWXuNsN2
=>**CONSTRUCTOR INVERSION/INJECTION**
	-> Pros and Cons ->https://prnt.sc/nU51h9BteZwe
	-> Example -> https://prnt.sc/aS-NpqGBZ7Fv
=>**PROPERTY INVERSION/INJECTION**
	-> Pros and Cons ->https://prnt.sc/AT7GoDFQrfMO
	-> Example -> https://prnt.sc/bpiSOyNBEw2U
=>**PARAMETER INVERSION/INJECTION**
	-> Pros and Cons ->https://prnt.sc/xv80ukHHXH_7
	-> Example -> https://prnt.sc/F5jOD5yfWt0K
	*НЕ Е ИНТУИТИВНО*, МНОГО ПОВЕЧЕ КОД...
->**КАКВО ДА СЕ ИЗБЯГВА** / Classic DIP Violations
	using "**new**"keyword
	using "**static**" methods/properties
->**How to fix code that violates DIP**
	**Extract interfaces** + use **constructor injection**
	Set up an Inversion of Control (IoC) container
 
---

==Adapter Pattern==
--
->Example 1
	https://prnt.sc/DtmmkFi8_TML pt1
	https://prnt.sc/gKJMSg2QYDck pt2
	
---

==Coupling==
--
 **Coupling** - the degree of dependence between modules 
	 How closely connected two modules are 
	 The strength of the relationship between modules 
 **Lose Coupling** means that the parts have minimal knowledge of each other and can work **independently**
	 Changes in one part are less likely to affect other parts, making the program more flexible and easier to modify
 **Tight Coupling** means that the parts are strongly connected and depend on each other's internal details
	 Changes in one part may require modifications in other tightly coupled parts, making the program more rigid and harder to be modified 
 Aim for **loose** coupling 

---

==Cohesion==
--
 **Cohesion** refers to how well the different parts of a program or module fit together and work towards a common goal
 **High Cohesion** means that the parts are closely related and focused on a specific task, making the code easier to understand and maintain
 **Low Cohesion** means that the parts are not strongly related and may have multiple responsibilities, which can make the code more complex and harder to work with
 Aim for **high cohesion** -> **modular and maintainable code**

=> Cohesive interface example: https://prnt.sc/AHPC6sPc5odJ