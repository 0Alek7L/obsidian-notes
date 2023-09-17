#OOP
Може да се наследява само от един клас!

**Superclass** - Parent class, Base class
    The class giving its **members** to its **child class**
**Subclass** - **Child** class, **Derived class**
	The class taking members from its base class

			  SUPERCLASS
				 / \
			     | |
			   SUBLCASS

Като има наследяване и базовият клас и наследяващият клас имат еднаква променлива в наследяващият клас се пише **this.variable** или **base.variable**!

Може да се наследяват променливи за методи като се сложи **based: (variable1, variable2..)**

При **override** на методи, първо се извиква child методът, а после ако е дописано се извиква и базовият. Използват се думите **override** и **virutal** https://prnt.sc/vq1DZT15uA3h

Думичката **sealed** предотвратява наследяването от мястото, на което е използвана. Мястото може да **method**, **property** в **base** клас


