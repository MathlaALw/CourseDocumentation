# List in CSharp

**definition**:
 Generic collection that provides dynamic array functionality.

**usage**:
it allows to store a collection of objects that can be accessed by index.
the last class provides methods to manipulate the collection, such as adding, removing, and searching for elements.

**Key features of List:**
- **Dynamic resizing:** Automatically adjusts its size as elements are added or removed.
- **Type safety:** Can be strongly typed to hold specific data types.
- **Indexing:** Elements can be accessed using an index, similar to arrays.
- **Rich API:** Provides methods for searching, sorting, and manipulating the collection.

**Creating a List:**
```
List<int> numbers = new List<int>();
```
**Adding elements:**
```
numbers.Add(1);
numbers.AddRange(new int[] { 2, 3, 4 });
```
**Accessing elements:**
```
int firstNumber = numbers[0]; // Accessing the first element
```
**Iterating through a List:**
it can be done using a `foreach` loop or a `for` loop.
```
// foreach loop
foreach (int number in numbers)
{
	Console.WriteLine(number);
}

// for loop
for (int i = 0; i < numbers.Count; i++)
{
	Console.WriteLine(numbers[i]);
}
```
**Removing elements:**
```
numbers.Remove(2); // Removes the first occurrence of 2
numbers.RemoveAt(0); // Removes the element at index 0
```
**Finding elements:**
```
bool containsThree = numbers.Contains(3); // Checks if 3 is in the list
int indexOfFour = numbers.IndexOf(4); // Gets the index of the first occurrence of 4
int filteredNumbers = numbers.Find(n => n > 2); //n -> value of the element -- n > 2 --> condition
```

**Checking:**
```
bool isEmpty = numbers.Count == 0; // Checks if the list is empty
bool isNotEmpty = numbers.Count > 0; // Checks if the list is not empty
```
**Sorting a List:**
```
numbers.Sort(); // Sorts the list in ascending order
```
**Counting elements:**
```
int count = numbers.Count; 
```
~~Note:~~

- **Foreach loop is slower than for loop.**


- Array and List have index so we use loop to access elements. -> **Faster**
- All the things that we can do with List we can do with Array. 

