# Queue in CSharp

**Definition:**
A Queue is a collection that follows the First In, First Out (FIFO) principle, 
meaning the first element added is the first one to be removed.

**Key Operations:**
- **Enqueue:** Adds an element to the end of the queue.
- **Dequeue:** Removes and returns the front element of the queue.
- **Peek:** Returns the front element without removing it.
- **Count:** Returns the number of elements in the queue.


**Example Usage:**
```
Queue<int> queue = new Queue<int>();
queue.Enqueue(1); // Adds 1 to the queue
queue.Enqueue(2); // Adds 2 to the queue
int frontElement = queue.Peek(); // Returns 1 without removing it
int dequeuedElement = queue.Dequeue(); // Removes and returns 1
```