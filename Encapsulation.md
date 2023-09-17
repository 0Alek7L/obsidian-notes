#OOP 
-> **ENCAPSULATION - A WAY OF HIDING IMPLEMENTATION AND REDUCING COMPLEXITY AND ENSURING THAT STRUCTURAL CHANGES REMAIN LOCAL**

->Може да се създаде в нов namespace проект от типа **Class Library**, което значи, че това е проект **без Main Method**! Той не се стартира, а само пази някакъв код. 

->**За да се направи референция от новия проект в новия namespace:**
solution explorer -> десен бутон на **Dependencies** -> **Add Project Reference**  и избираме към кой проект да се направи референция

->**internal** позволява ползването на класа само в текущият проект. Ако има референция към друг проект и в сегашния е използван **internal**, този клас е достъпен само в текущия проект, но не в този с референция!

->Ако искаме класът да е **read-only** трябва да сложим **private setters**:
	public int Age = {get; **private set;**}

->Ако искаме да можем да задаваме стойност на property само при инициализация или в конструктор може да махнем setter-а. Така не може да се зададе стойност извън класа и става **read-only property**
	public int Age = {get;}

->functional programming implementation in methods -> https://prnt.sc/rtSDA6uDz6ob

->**IReadOnlyCollection** usage -> https://prnt.sc/R4eWMGO-ZKPP
	 
