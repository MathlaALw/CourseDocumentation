# *Algorithm programming components*

 **Algorithm** -> A set of instructions that are followed in order to solve a problem.it consist of Finite ,well defined and ordered insteructions.

 ## characteristics of a good algorithm:

 1. **Correctness** -> It should produce the correct result.
2. **Efficiency** -> It should be efficient in terms of time and space.
3. **Finiteness** -> It should terminate after a finite number of steps.
4. **Generality** -> It should be applicable to a range of problems.
5. **Clarity** -> It should be clear and easy to understand.

## Components of an algorithm:

1. **Variables** -> It is a memory location that holds a value.
    ```	
    
     int a = 5;
	float b = 3.14;
	char c = 'A';
	string d = "Hello";
	bool e = true;
	
	```
2. **Input and Output** -> It is the data that is given to the algorithm and the data that is produced by the algorithm.
		
		
		string name 
		print " Enter your Name :" 
		input name
		print "Your name is : " ,name
	
3. **Conditional Statements** -> It is a statement that performs different actions based on whether a condition is true or false.
	- **If-Else Statement** -> It is a statement that executes a block of code if a condition is true, and another block of code if the condition is false.
		
		```
		int age;
		print "Enter your age :"
		input age

		if(age >= 18)
		{
			print "You are an adult"
		}
		else
		{
			print "You are a child"
		}
		```
	- **Nested If-Else Statement** -> It is an if-else statement inside another if-else statement.
		```
		int marks;
		print "Enter your marks :"
		input marks
		if (marks >= 90)
		{
			print "Grade A"
		}
		else if (marks >= 80)
		{
			print "Grade B"
		}
		else if (marks >= 70)
		{
			print "Grade C"
		}
		else
		{
			print "Fail"
		}
		```


4. **Loops** -> It is a sequence of instructions that is continually repeated until a certain condition is reached.
	- **For Loop** -> It is a loop that executes a block of code a specified number of times.
		```
		for (int i = 0; i < 5; i++)
		{
			print i
		}
		```
	- **While Loop** -> It is a loop that executes a block of code as long as a condition is true.
		```

		int i = 0;
		while (i < 5)
		{
			print i
			i++
		}
		```

	- **Do-While Loop** -> It is a loop that executes a block of code at least once, and then repeats the loop as long as a condition is true.
		```

		int i = 0;
		do
		{
			print i
			i++
		} while (i < 5);
		```

5. **Arrays** -> It is a collection of elements that are stored in a contiguous memory location.
	- **One-Dimensional Array** -> It is an array that stores elements in a single row.
		```
		int[] numbers = {1, 2, 3, 4, 5};
		```
	- **Two-Dimensional Array** -> It is an array that stores elements in rows and columns.
		```
		int[,] matrix = {{1, 2}, {3, 4}, {5, 6}};
		```
		Example :
		- Sorting Numbers in an array
		```

		int[] numbers = {5, 3, 8, 1, 2};

		for (int i = 0; i < numbers.Length; i++)
		{
			for (int j = i + 1; j < numbers.Length; j++)
			{
				if (numbers[i] > numbers[j])
				{
					int temp = numbers[i];
					numbers[i] = numbers[j];
					numbers[j] = temp;
				}
			}
		} 		
	 
	   output : 1,2,3,5,8
		```
		or 
		
		```
		numbers = {1, 2, 3, 5, 8}
		print numbers[3] 
		----
		output : 5
		```
		- looping through an array
		```
		number = {1, 2, 3, 4, 5}
		for (int i = 0; i < numbers.Length; i++)
		{
			print numbers[i]
		}
		output: 1,2,3,4,5
		```
	

6. **Functions** -> It is a block of code that performs a specific task.(Reusable block of code).
	
	- **built-in functions** -> It is a function that is provided by the programming language.
		```
		print("Hello, World!");
		```
	- **user defined functions** -> It is a function that is created by the user.
		```
		int add(int a, int b)
		{
			return a + b;
		}
		```
		Example:
		- **Function to add two numbers**
		
			```
			function add(a, b)
			{
				return a + b
			}
			```

# **Summary** :

|Concept|Purpose|Example|
|-------|-------|-------|
|Variables|It is a memory location that holds a value.|int a = 5;|
|Input and Output|It is the data that is given to the algorithm and the data that is produced by the algorithm.|print "Enter your Name :"|
|Conditional Statements|It is a statement that performs different actions based on whether a condition is true or false.|if(age >= 18)|
|Loops|It is a sequence of instructions that is continually repeated until a certain condition is reached.|for (int i = 0; i < 5; i++)|
|Arrays|It is a collection of elements that are stored in a contiguous memory location.|int[] numbers = {1, 2, 3, 4, 5};|
|Functions|It is a block of code that performs a specific task.|int add(int a, int b)|
