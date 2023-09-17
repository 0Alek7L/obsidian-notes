#Advanced 
**STACK**

**Stack** implements a **LIFO**(last in, first out) collection
- **Push**: insert an element at the top of the stack
- **Pop**: take the element from the top of the stack
- **Peek**: retrieve the topmost element without removing it
- .ToArray()
- .Contains()
- .Clear()
- .TrimExcess() - shrink the internal array
---

	Stack<int> numbers = new();
	numbers.Push(10);//add
	numbers.Push(20);/add
	int num2 = numbers.Peek();//will set the variable's value to 5 but will not remove anything
	numbers.Push(5);/add
	int number = numbers.Pop();//removes 5 from the stack and sets the variable's value to 5

---
**QUEUE**

**Queue** implements a FIFO(first in, first out) collection
- Enqueue: append an element at the end of the queue
- Dequeue: remove the first element from the queue
- Peek: retrieve the first element of the queue without removing it

---

	Queue<string> names = new(new string[] {"niki", "hektor", "stoqn"});
    string currentName = names.Dequeue();
    names.Enqueue(currentName);
    //this reverses the queue

**queue.Enqueue(queue.Dequeue());**//puts the first element at the end