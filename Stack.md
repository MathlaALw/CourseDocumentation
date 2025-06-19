# Stack in CSharp

**definition:**

A Stack is a collection that follows the Last In, First Out (LIFO) principle, 
meaning the last element added is the first one to be removed.

generic stack -> it can hold any type of data.

**Key Operations:**
- **Push:** Adds an element to the top of the stack.
- **Pop:** Removes and returns the top element of the stack.
- **Peek:** Returns the top element without removing it.
- **Count:** Returns the number of elements in the stack.

**Example Usage:**
```
Stack<int> stack = new Stack<int>();
stack.Push(1); // Adds 1 to the stack
stack.Push(2); // Adds 2 to the stack
int topElement = stack.Peek(); // Returns 2 without removing it
int poppedElement = stack.Pop(); // Removes and returns 2
```
