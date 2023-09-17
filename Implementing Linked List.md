#Advanced 
**VERY FAST AND USEFUL**

Every LinkedList has head, node/s and tail

	10(head)->20(node)->30(node)->40(tail)

	Node head;
	head.Next //20
	head.Next.Next //30

-------------------

	LinkedList<int> linkedList = new();
	linkedList.AddLast(10);
	linkedList.AddLast(20);
	linkedList.AddLast(30);
	linkedList.AddLast(40);
	Console.WriteLine(linkedList.First.Value);//10
	Console.WriteLine(linkedList.Last.Value);//40

------

**Node**
- Value
- Node Next
- Node Previous 

**LinkedList**
- Node Head
- Node Tail
- Add Last/First
- Remove Last/First

-----

Обхождане:

	LinkedListNode<int> currentNode = linkedList.First;
	while(currentNode!=null)
	{
		Console.WriteLine(currentNode.Value);
		currentNode = currentNode.Next;
	}

---

	public class Node
    {
        public Node(int value, Node next=null, Node previous=null)
        {
            Value = value;
            Next = next;
            Previous = previous;
        }

        public int Value { get; set; }
        public Node Next { get; set; }
        public Node Previous { get; set; }
    }
	internal class Program
    {
        static void Main(string[] args)
        {
            Node ten = new Node(10);//adding 10
            Node twenty = new Node(20);/adding 20
            ten.Next = twenty;//now 10 knows what follows after
            twenty.Previous = ten;//now 20 knows what sits before 
        }
    }

----

