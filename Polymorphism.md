#OOP 

**Това е част от ООП принципите, която ни позволява един клас/обект да приема много форми

пример: https://prnt.sc/uFntvHoy5HR8

ВИДОВЕ ПОЛИМОРФИЗЪМ
--
->**COMPILE-TIME POLYMORPHISM**
	също познат като статичен полиморфизъм
	когато параметрите могат да варират по:
		-брой
		-data type
		-подредба (int, double/double, int)
	EXAMPLE: https://prnt.sc/78Wfi-BB9ZBV -> постигнат чрез overloading на методи

OVERRIDE VS OVERLOAD
--
OVERLOAD -> COMPILE-TIME POLYMORPHISM
OVERRIDE -> RUN-TIME POLYMORPHISM


CASTING
--
	Animal dog = new Dog();
	Dog myDog = dog as Dog; //return null => safe casting
	Dog myDog2 = (Dog)dog; //Exception => unsafe casting

---
OVERRIDING
--
За да се override-не един обект той трябва да е abstract или virtual

