# Files in CSharp

**Definition:**
A File is a collection of data stored on a storage device, such as a hard drive or SSD.
Files can be text files, binary files, images, or any other type of data. In C#, the `System.IO` namespace provides classes for working with files.

**Read from a File:**
```
using System.IO;
string filePath = "example.txt";
if (File.Exists(filePath))
{
	string content = File.ReadAllText(filePath);
	Console.WriteLine(content);
}
else
{
	Console.WriteLine("File does not exist.");
}
```

**Create a File:**
```
using System.IO;
string filePath = "newfile.txt";
File.WriteAllText(filePath, "Hello, World!");
Console.WriteLine("File created successfully.");
```

**Write to a File:**
```
using System.IO;
string filePath = "example.txt";
File.AppendAllText(filePath, "\nNew line added.");
Console.WriteLine("Text appended to file.");
```
- **Write to a File without deleting existing content using streamWriter:**
```
using System.IO;
string filePath = "example.txt";
using (StreamWriter writer = new StreamWriter(filePath, true))
{
	writer.WriteLine("Another line added.");
}
Console.WriteLine("Text appended to file using StreamWriter.");
```
- **Write to a File adding multiple lines:**
```
using System.IO;
string filePath = "example.txt";
using (StreamWriter writer = new StreamWriter(filePath, true))
{
	writer.WriteLine("First line.");
	writer.WriteLine("Second line.");
	writer.WriteLine("Third line.");
}
Console.WriteLine("Multiple lines added to file using StreamWriter.");
```

**Delete a File:**
```
using System.IO;
string filePath = "example.txt";
if (File.Exists(filePath))
{
	File.Delete(filePath);
	Console.WriteLine("File deleted successfully.");
}
else
{
	Console.WriteLine("File does not exist.");
}
```

