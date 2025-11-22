# JavaScript Fundamentals

## what is JavaScript?

JavaScript is a versatile, high-level programming language primarily used for web development. It enables developers to create interactive and dynamic content on websites, such as animations, form validations, and user interface enhancements. JavaScript can be executed on both the client-side (in the browser) and server-side (using environments like Node.js). It is an essential technology alongside HTML and CSS for building modern web applications.

## the three type of JavaScript:

1. **inline** -> This type of JavaScript is written directly within an HTML element using the `onclick`, `onmouseover`, or other event attributes. It is typically used for simple tasks and quick interactions.
```html
<button onclick="alert('Hello, World!')">Click Me</button>
```

2. **internal** -> This type of JavaScript is written within a `<script>` tag in the `<head>` or `<body>` section of an HTML document. It is useful for adding scripts that are specific to that particular page.
```html
<!DOCTYPE html>
<html>
<head>
	<script>
		function showMessage() {
			alert('Hello from internal JavaScript!');
		}
	</script>
	</head>
	<body>
	<button onclick="showMessage()">Click Me</button>
	</body>
	</html>
```
3. **external** -> This type of JavaScript is written in a separate `.js` file and linked to the HTML document using the `<script>` tag with the `src` attribute. This approach is preferred for larger scripts and promotes code reusability.
	
```html
	<!DOCTYPE html>
	<html>
	<head>
		<script src="script.js"></script>
		</head>
		<body>
		<button onclick="showMessage()">Click Me</button>
		</body>
		</html>
		

// script.js
function showMessage() {
	alert('Hello from external JavaScript!');
}
```

## 

### Declarations:
In JavaScript, variables can be declared using three keywords: `var`, `let`, and `const`.
- `var`: This keyword is used to declare a variable that can be re-assigned and has function scope. It is the oldest way to declare variables in JavaScript.
```javascript
var name = "John";
name = "Doe"; // re-assignment is allowed
console.log(name); // Output: Doe
```

- `let`: This keyword is used to declare a block-scoped variable that can be re-assigned. It is the preferred way to declare variables in modern JavaScript.
```javascript
let age = 25;
age = 26; // re-assignment is allowed
console.log(age); // Output: 26
```

- `const`: This keyword is used to declare a block-scoped variable that cannot be re-assigned. It is used for values that should remain constant throughout the program.
```javascript
const pi = 3.14;
// pi = 3.14159; // This will throw an error
console.log(pi); // Output: 3.14
```
## Comparison of `var`, `let`, and `const`:

|                | var		    | let           | const         |
|----------------|--------------|---------------|---------------|
| Redeclaration  | Allowed      | Not Allowed   | Not Allowed   |
| Re-assignment  | Allowed      | Allowed       | Not Allowed   |
| Hoisting       | Yes          | Yes           | Yes           |
| Scope          | Function     | Block         | Block         |

### Data Types:
JavaScript has several built-in data types, including:
- **Primitive Data Types**:
  - `Number`: Represents both integer and floating-point numbers.
	```javascript
	let num = 42;
	let floatNum = 3.14;
	```
  - `String`: Represents a sequence of characters.
	```javascript
	let str = "Hello, World!";
	```
  - `Boolean`: Represents a logical entity that can be either `true` or `false`.
	```javascript
	let isTrue = true;
	let isFalse = false;
	```
  - `Undefined`: Represents a variable that has been declared but not assigned a value.
	```javascript
	let undef;
	console.log(undef); // Output: undefined
	```
  - `Null`: Represents the intentional absence of any object value.
	```javascript
	let emptyValue = null;
	```
  - `NaN`: Represents a value that is "Not-a-Number".
	```javascript
	let notANumber = NaN;
	```
	
## Operators:

JavaScript provides various operators for performing operations on variables and values. Some common operators include:

- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
```javascript
let a = 10;
let b = 5;
let sum = a + b; // 15
let difference = a - b; // 5
let product = a * b; // 50
let quotient = a / b; // 2
let remainder = a % b; // 0
```

- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`
```javascript
let x = 10;
x += 5; // x = x + 5 -> 15
x -= 3; // x = x - 3 -> 12
x *= 2; // x = x * 2 -> 24
x /= 4; // x = x / 4 -> 6
```

- **Comparison Operators**: `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`
```javascript
let isEqual = (5 == '5'); // true (loose equality)
let isStrictEqual = (5 === '5'); // false (strict equality)
let isNotEqual = (5 != 10); // true
let isGreater = (10 > 5); // true
let isLessOrEqual = (5 <= 5); // true
```

- **Logical Operators**: `&&`, `||`, `!`
```javascript
let andResult = (true && false); // false
let orResult = (true || false); // true
let notResult = !true; // false
```

#### Truth table for Logical Operators:
| A     | B     | A && B | A OR B | !A    |
|-------|-------|--------|--------|-------|
| true  | true  | true   | true   | false |
| true  | false | false  | true   | false |
| false | true  | false  | true   | true  |
| false | false  | false  | false | true  |


### Control Structures:
JavaScript provides various control structures to manage the flow of execution in a program. Some common control structures include:


- **Loops**: `for`, `while`, `do...while`
```javascript

// for loop
for (let i = 0; i < 5; i++) {
	console.log(i); // Output: 0, 1, 2, 3, 4
}



// while loop
let j = 0;
while (j < 5) {
	console.log(j); // Output: 0, 1, 2, 3, 4
	j++;
}


// do...while loop
let k = 0;
do {
	console.log(k); // Output: 0, 1, 2, 3, 4
	k++;
} while (k < 5);
```

	


- **Conditional Statements**: `if`, `else if`, `else`, `switch`
```javascript

// if...else if...else
let grade = 85;
if (grade >= 90) {
	console.log("A");
} else if (grade >= 80) {
	console.log("B");
} else if (grade >= 70) {
	console.log("C");
} else {
	console.log("F");
}
```
  - **Ternary Operator**: A shorthand for `if...else` statements.
	```javascript
	if name == "Salim" ? console.log("Hello, Salim!") : console.log("Hello, Guest!");
	```

	~~NOTE:~~ we can use ternary operator only for simple conditions thet return single value.







## Switch Case:

### What is Switch Case?

Switch case is a control statement used to compare one value against multiple possible cases.

### Syntax of switch case:
```javascript
switch (expression) {
  case value1:
	// code to be executed if expression === value1
	break;
  case value2:
	// code to be executed if expression === value2
	break;
  ...
  default:
	// code to be executed if expression doesn't match any case
}
```


### The parts of switch case:

1. **expression**: This is the value you want to test.

2. **case value**: Each possible match.

3. **break**: Stops the switch from continuing to the next case.
Without break, JavaScript will continue reading the next cases (called fall-through).

4. **default**: Runs if no cases matched.

### Example of switch case:
```javascript

let day = 3;
switch (day) {
  case 1:
	console.log("Monday");
	break;
  case 2:
	console.log("Tuesday");
	break;
  case 3:
	console.log("Wednesday");
	break;
  case 4:
	console.log("Thursday");
	break;
  case 5:
	console.log("Friday");
	break;
  case 6:
	console.log("Saturday");
	break;
  case 7:
	console.log("Sunday");
	break;
  default:
	console.log("Invalid day");
}
```

### Output:
```
Wednesday
```

### Without break (fall-through example):
```javascript
let color = "red";
switch (color) {
  case "red":
	console.log("Color is red");
  case "blue":
	console.log("Color is blue");
  case "green":
	console.log("Color is green");
  default:
	console.log("Unknown color");
}
```
### Output:
```
Color is red
Color is blue
Color is green
Unknown color
```



### When to use switch case:

- When you have multiple possible values for a single variable.

- your conditions are based on equality checks.


### When to use if else:
- When your conditions involve ranges . (e.g., greater than, less than).)
- When you need to evaluate different variables or expressions.
