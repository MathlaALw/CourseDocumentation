# *Foundamentals of programming in Csharp*


1. **Basic Structure of a C# Program**
	- **Namespace** -> It is a collection of classes.
	- **Class** -> It is a blueprint for creating objects.
	- **Method** -> It is a block of code that performs a specific task.
	- **Statement** -> It is an instruction that tells the computer to perform a specific action.


	```	using System; // Importing built-in namespace
     namespace MyFirstApp // Namespace declaration
    {
      class Program // Class declaration
      {
         static void Main() // Main method (Entry point of the program)
         {
             Console.WriteLine("Hello, World!"); // Print statement
         }
      }
     }
	```

2. **Comments in C#** -> help to document the code and make it more readable.
	- **Single Line Comment** -> It is used to comment a single line of code.
		```
	    // This is a single line comment
	    ```
	- **Multi-Line Comment** -> It is used to comment multiple lines of code.
		```
		/*
		This is a
		multi-line
		comment
		*/
		```
	- **XML Documentation Comment** -> It is used to generate documentation for the code.
		```
		/// <summary>
		/// This is a summary of the method.
		/// </summary>
		/// static void Greet()			
	        {
               Console.WriteLine("Hello!");
            }
		```


3. **Data types**
- **Value Type**

|Type|Size|Example|
|----|----|-------|
|int|4 bytes|int age = 25;|
|float|4 bytes|float salary = 5000.50;|
|double|8 bytes|double pi = 3.14159;|
|char|2 bytes|char grade = 'A';|
|bool|1 byte|bool isAdult = true;|

	
- **Reference Type**

|Type|Size|Example|
|----|----|-------|
|string|Depends on the string length|string name = "John";|


4. **Input / Output**

	```
	Console.WriteLine("Enter your age :");
	
	nage=float.Parse(Console.ReadLine());

	Console.WriteLine(age);
	Console.WriteLine("Your age is : " + age);
	```
	
5. **Operator**
	- **Arithmetic Operators**
	
		|Operator|Description|Example|
		|--------|-----------|-------|
		|+|Addition|a + b|
		|-|Subtraction|a - b|
		|*|Multiplication|a * b|
		|/|Division|a / b|
		|%|Modulus|a % b|
	
		
	- **Logical Operators**
		
		|Operator|Description|Example|
		|--------|-----------|-------|
		|&&|Logical AND|a && b|
		|!!| Logical OR|a !! b|
		|!|Logical NOT|!a|
		|<|Less than|a < b|
		|>|Greater than|a > b|
		|<=|Less than or equal to|a <= b|
		|>=|Greater than or equal to|a >= b|
		|==|Equal to|a == b|
		|!=|Not equal to|a != b|
		
		
6. **Conditional**
	- **If-Else Statement**
		```
		int age;
		Console.WriteLine("Enter your age :");
		age = int.Parse(Console.ReadLine());
	
		if(age >= 18)
		{
			Console.WriteLine("You are an adult");
		}
		else
		{
			Console.WriteLine("You are a child");
		}
		```
	- **Switch Statement**
		```
		int day;
		Console.WriteLine("Enter the day number :");
		day = int.Parse(Console.ReadLine());
	
		switch(day)
		{
			case 1:
				Console.WriteLine("Sunday");
				break;
			case 2:
				Console.WriteLine("Monday");
				break;
			case 3:
				Console.WriteLine("Tuesday");
				break;
			case 4:
				Console.WriteLine("Wednesday");
				break;
			case 5:
				Console.WriteLine("Thursday");
				break;
			case 6:
				Console.WriteLine("Friday");
				break;
			case 7:
				Console.WriteLine("Saturday");
				break;
			default:
				Console.WriteLine("Invalid day number");
				break;
		}
		```
7. **Loop**
	- **For Loop**
		```
		int i;
		for(i=1; i<=5; i++)
		{
			Console.WriteLine(i);
		}
		```
	- **While Loop**
		```
		int i = 1;
		while(i<=5)
		{
			Console.WriteLine(i);
			i++;
		}
		```
	- **Do-While Loop**
		```
		int i = 1;
		do
		{
			Console.WriteLine(i);
			i++;
		}while(i<=5);
		```
	- **forech loop**
		```
		string[] fruits = { "Apple", "Banana", "Cherry" };
        foreach (string fruit in fruits)
        {
            Console.WriteLine(fruit);
        }

		```
8. **Nested operations**
	- **Nested Condition** (Nested IF-Else)
		```
		int marks;
		Console.WriteLine("Enter your marks :");
		marks = int.Parse(Console.ReadLine());
		if(marks >= 90)
		{
			Console.WriteLine("Grade A");
		}
		else if(marks >= 80)
		{
			Console.WriteLine("Grade B");
		}
		else if(marks >= 70)
		{
			Console.WriteLine("Grade C");
		}
		else
		{
			Console.WriteLine("Fail");
		}
		```
	- **Nested Loop** (Nested For Loop)
		```
		int i, j;
		for(i=1; i<=5; i++)
		{
			for(j=1; j<=i; j++)
			{
				Console.Write("*");
			}
			Console.WriteLine();
		}
		```

9. **Arrays** -> a collection of elements that are stored in a contiguous memory location.
#### **Key Feature of Array**

1. Fixed size -> The size of the array is fixed and cannot be changed.
2. Same data type -> All elements in the array must be of the same data type.
3. Index -> Each element in the array is accessed by its index.
4. Efficient access -> Elements in the array can be accessed efficiently using the index.

### Declaring and Initializing Arrays
### ( *One-Dimensional Array* )
1. **Declaring an Array**
	- Syntax: `data_type[] array_name;`
	   
	
		```
		int[] numbers;
		```

2. **Initializing an array**
	- Syntax: `data_type[] array_name= new data_type[];`
	- Example:
 
	```
	int[] numbers = new int[5]; //Initializes an array with 5 elements, all set to 0 by default
	int[] numbers = new int[] { 1, 20, 13, 4, 5 }; // Initializes an array with the values 1, 2, 3, 4, 
	```

3. **Accessing Array Elements**
	- Syntax: `array_name[index]`
	- Example:
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		Console.WriteLine(numbers[0]); // Output: 1
		Console.WriteLine(numbers[1]); // Output: 2
		```

4. **Modifying Array Elements**
	- Syntax: `array_name[index] = value;`
	- Example:
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		numbers[0] = 10;
		Console.WriteLine(numbers[0]); // Output: 10
		```
5. **Iterating Over an Array**
	- **For Loop**
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		for (int i = 0; i < numbers.Length; i++)
		{
			Console.WriteLine(numbers[i]);
		}
		```
	- **Foreach Loop**
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		foreach (int number in numbers)
		{
			Console.WriteLine(number);
		}
		```

### ( *Two-Dimensional Array* )
1. **Declaring a Two-Dimensional Array**
	- Syntax: `data_type[,] array_name;`
	- Example:
	
		```
		int[,] matrix;
		```
2. **Initializing a Two-Dimensional Array**
	- Syntax: `data_type[,] array_name = new data_type[row_count, column_count];`
	- Example:
	
		```
		int[,] matrix = new int[3, 2]; // Initializes a 3x2 matrix
		```
3. **Accessing Two-Dimensional Array Elements**
	- Syntax: `array_name[row_index, column_index]`
	- Example:
	
		```
		int[,] matrix = { { 1, 2 }, { 3, 4 }, { 5, 6 } };
		Console.WriteLine(matrix[0, 0]); // Output: 1
		Console.WriteLine(matrix[1, 1]); // Output: 4
		```

### ( *Jagged Array* )
1. **Declaring a Jagged Array**
	- Syntax: `data_type[][] array_name;`
	- Example:
	
		```
		int[][] jaggedArray;
		```
2. **Initializing a Jagged Array**
	- Syntax: `data_type[][] array_name = new data_type[row_count][];`
	- Example:
	
		```
		int[][] jaggedArray = new int[3][];
		jaggedArray[0] = new int[] { 1, 2, 3 };
		jaggedArray[1] = new int[] { 4, 5 };
		jaggedArray[2] = new int[] { 6, 7, 8, 9 };
		```
3. **Accessing Jagged Array Elements**
	- Syntax: `array_name[row_index][column_index]`
	- Example:
	
		```
		int[][] jaggedArray = new int[3][];
		jaggedArray[0] = new int[] { 1, 2, 3 };
		jaggedArray[1] = new int[] { 4, 5 };
		jaggedArray[2] = new int[] { 6, 7, 8, 9 };
		Console.WriteLine(jaggedArray[0][1]); // Output: 2
		Console.WriteLine(jaggedArray[2][2]); // Output: 8
		```
## Array Methods and Properties

1. **Length Property**
	- Syntax: `array_name.Length`
	- Example:
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		Console.WriteLine(numbers.Length); // Output: 5
		```

2. **IndexOf Method**
 	- Syntax: `Array.IndexOf(array_name, value);`
	- Example:
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		Console.WriteLine(Array.IndexOf(numbers, 3)); // Output: 2
		```
3. **Sort Method**
	- Syntax: `Array.Sort(array_name);`
	- Example:
	
		```
		int[] numbers = { 5, 3, 8, 1, 2 };
		Array.Sort(numbers);
		foreach (int number in numbers)
		{
			Console.WriteLine(number);
		}
		```
4. **Reverse Method**
	- Syntax: `Array.Reverse(array_name);`
	- Example:
	
		```
		int[] numbers = { 1, 2, 3, 4, 5 };
		Array.Reverse(numbers);
		foreach (int number in numbers)
		{
			Console.WriteLine(number);
		}
		```

## Functions in CSharp 
- **There are two types of Functions:** 
	1. **Built-in Functions** -> It is a function that is provided by the programming language.
		a. **Math Functions** -> It is a function that performs mathematical operations.
			
			- **Math.Abs()** -> Returns the absolute value of a number.
			
				```
				Console.WriteLine(Math.Abs(-5)); // Output: 5
				```
			
			- **Math.Max()** -> Returns the larger of two numbers.
				
				```
				Console.WriteLine(Math.Max(10, 20)); // Output: 20
				```
			
			- **Math.Min()** -> Returns the smaller of two numbers.
				
				```
				Console.WriteLine(Math.Min(10, 20)); // Output: 10
				```
			
			- **Math.Sqrt()** -> Returns the square root of a number.
				
				```
				Console.WriteLine(Math.Sqrt(25)); // Output: 5
				```

			- **Math.Pow()** -> Returns a specified number raised to the specified power.
				
				```
				Console.WriteLine(Math.Pow(2, 3)); // Output: 8
				```
			
			- **Math.Round()** -> Rounds a number to the nearest integer.
				
				```
				Console.WriteLine(Math.Round(3.5)); // Output: 4
				```
			
		 b. **String Functions** -> It is a function that performs operations on strings.
			
			- **String.Length** -> Returns the length of a string.
				
				```
				string name = "John";
				Console.WriteLine(name.Length); // Output: 4
				```
			
			- **String.ToUpper()** -> Converts a string to uppercase.
				
				```
				string name = "John";
				Console.WriteLine(name.ToUpper()); // Output: JOHN
				```
			
			- **String.ToLower()** -> Converts a string to lowercase.
				
				```
				string name = "JOHN";
				Console.WriteLine(name.ToLower()); // Output: john
				```
			
			- **String.Contains()** -> Checks if a string contains a specified value.
				
				```
				string name = "John";
				Console.WriteLine(name.Contains("o")); // Output: True
				```
			
			- **String.Substring()** -> Extracts a substring from a string.
				
				```
				string name = "John";
				Console.WriteLine(name.Substring(1, 2)); // Output: oh
				```
			
			- **String.Replace()** -> Replaces a specified value in a string.
				
				```
				string name = "John";
				Console.WriteLine(name.Replace("J", "M")); // Output: Monn
				```
			
			- **String.Split()** -> Splits a string into an array of substrings.
				
				```
				string names = "John, Jane, Jack";
				string[] nameArray = names.Split(',');
				foreach (string name in nameArray)
				{
					Console.WriteLine(name);
				}
				```
			
			- **String.Trim()** -> Removes whitespace from the beginning and end of a string.
				
				```
				string name = " John ";
				Console.WriteLine(name.Trim()); // Output: John
				```
			
		c. **Date and Time Functions** -> It is a function that performs operations on dates and times.
		
			- **DateTime.Now** -> Returns the current date and time.
			
				```
				Console.WriteLine(DateTime.Now); // Output: 10/10/2021 12:00:00 AM
				```
			
			- **DateTime.Today** -> Returns the current date.
			
				```
				Console.WriteLine(DateTime.Today); // Output: 10/10/2021 12:00:00 AM
				```
			
			- **DateTime.AddDays()** -> Adds a specified number of days to a date.
			
				```
				DateTime date = DateTime.Today;
				Console.WriteLine(date.AddDays(7)); // Output: 10/17/2021 12:00:00 AM
				```
			
			- **DateTime.ToString()** -> Converts a DateTime object to a string representation.
			
				```
				DateTime date = DateTime.Today;
				Console.WriteLine(date.ToString("MM/dd/yyyy")); // Output: 10/10/2021
				```
			
			- **DateTime.Parse()** -> Converts a string representation of a date and time to a DateTime object.
			
				```
				string dateString = "10/10/2021";
				DateTime date = DateTime.Parse(dateString);
				Console.WriteLine(date); // Output: 10/10/2021 12:00:00 AM
				```
			
			- **DateTime.TryParse()** -> Converts a string representation of a date and time to a DateTime object and returns a Boolean value indicating whether the conversion succeeded.
			
				```
				string dateString = "10/10/2021";
				DateTime date;
				if (DateTime.TryParse(dateString, out date))
				{
					Console.WriteLine(date); // Output: 10/10/2021 12:00:00 AM
				}
				else
				{
					Console.WriteLine("Invalid date");
				}
				```
			
		d. **Array Functions** -> It is a function that performs operations on arrays.
			
			- **Array.Sort()** -> Sorts the elements of an array.
			
				```
				int[] numbers = { 5, 3, 8, 1, 2 };
				Array.Sort(numbers);
				foreach (int number in numbers)
				{
					Console.WriteLine(number);
				}
				```
			
			- **Array.Reverse()** -> Reverses the order of the elements in an array.
			
				```
				int[] numbers = { 1, 2, 3, 4, 5 };
				Array.Reverse(numbers);
				foreach (int number in numbers)
				{
					Console.WriteLine(number);
				}
				```
			
			- **Array.IndexOf()** -> Searches for the specified object and returns the index of the first occurrence within the entire array.
			
				```
				int[] numbers = { 1, 2, 3, 4, 5 };
				Console.WriteLine(Array.IndexOf(numbers, 3)); // Output: 2
				```
			
			- **Array.Resize()** -> Changes the number of elements in an array to a specified new size.
			
				```
				int[] numbers = { 1, 2, 3, 4, 5 };
				Array.Resize(ref numbers, 3);
				foreach (int number in numbers)
				{
					Console.WriteLine(number);
				}
				```
			
		e. **Console Functions** -> It is a function that performs operations on the console.
			
			- **Console.WriteLine()** -> Writes the specified data, followed by the current line terminator, to the standard output stream.
			
				```
				Console.WriteLine("Hello, World!");
				```
			
			- **Console.ReadLine()** -> Reads the next line of characters from the standard input stream.
			
				```
				string name = Console.ReadLine();
				Console.WriteLine("Hello, " + name);
				```
			
			- **Conlose.Write()** -> Writes the specified data to the standard output stream.
			
				```
				Console.Write("Hello, World!");
				```
			
		f. **Type Conversion Functions** -> It is a function that performs type conversion.
			- **Convert.ToInt32()** -> Converts the specified value to a 32-bit signed integer.
			
				```
				string numberString = "123";
				int number = Convert.ToInt32(numberString);
				Console.WriteLine(number); // Output: 123
				```
			
			- **Convert.ToDouble()** -> Converts the specified value to a double-precision floating-point number.
			
				```
				string numberString = "123.45";
				double number = Convert.ToDouble(numberString);
				Console.WriteLine(number); // Output: 123.45
				```
			
			- **Convert.ToString()** -> Converts the specified value to its equivalent string representation.
		
				```
				int number = 123;
				string numberString = Convert.ToString(number);
				Console.WriteLine(numberString); // Output: 123
				```
			
			- **int.Parse and int.TryParse** -> Converts the string representation of a number to its 32-bit signed integer equivalent.
			
				```
				string numberString = "123";
				int number = int.Parse(numberString);
				Console.WriteLine(number); // Output: 123
				```
				```
				string numberString = "123";
				int number;
				if (int.TryParse(numberString, out number))
				{
					Console.WriteLine(number); // Output: 123
				}
				else
				{
					Console.WriteLine("Invalid number");
				}
				```
			
		g. **Random Number Functions** -> It is a function that generates random numbers.
			- **Random.Next()** -> Returns a non-negative random integer.
			
				```
				Random random = new Random();
				int number = random.Next();
				Console.WriteLine(number);
				```
			- **Random.Next(min, max)** -> Returns a random integer that is within a specified range.
			
				```
				Random random = new Random();
				int number = random.Next(1, 10);
				Console.WriteLine(number);
				```
			- **Random.NextDouble()** -> Returns a random floating-point number that is greater than or equal to 0.0 and less than 1.0.
			
				```
				Random random = new Random();
				double number = random.NextDouble();
				Console.WriteLine(number);
				```
	-----------------------------------------------------

## Errors in programming

1. **Syntax Errors** -> Errors that occur when the rules of the programming language are not followed.
	- Example:
		```
		int x = 5;
		Console.WriteLine(x)
		```
		**Error**: Missing semicolon at the end of the statement.
	- 
2. **Runtime Errors** -> Errors that occur during the execution of the program.
	- Example:
		```
		int x = 5;
		int y = 0;
		int z = x / y;
		```
		**Error**: Division by zero.



3. **Logical Errors** -> Errors that occur when the program does not produce the expected output.
	- Example:
		```
		int x = 5;
		int y = 3;
		int z = x - y;
		Console.WriteLine("The result is: " + z);
		```
		**Error**: The subtraction operator should be changed to the addition operator.

how to handle errors in programming:
1. **Try-Catch Block** -> It is used to handle exceptions that occur during the execution of the program.
	- Syntax:
		```
		try
		{
			// Code that may throw an exception
		}
		catch (Exception ex)
		{
			// Code to handle the exception
		}
		```
	- Example:
		```
		try
		{
			int x = 5;
			int y = 0;
			int z = x / y;
			Console.WriteLine("The result is: " + z);
		}
		catch (DivideByZeroException ex)
		{
			Console.WriteLine("Error: Division by zero");
		}
		```
2. **Validations** -> It is used to check the input data before processing it.
	- Example:
		```
		int age;
		Console.WriteLine("Enter your age:");
		if (int.TryParse(Console.ReadLine(), out age))
		{
			Console.WriteLine("Your age is: " + age);
		}
		else
		{
			Console.WriteLine("Invalid input");
		}
		```

