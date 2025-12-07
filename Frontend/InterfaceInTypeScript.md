# Interface in TypeScript


## What is an interface in TypeScript?

An interface in TypeScript is a contract or blueprint that defines the structure (shape) an object, class, or function must follow.

In simple words:

**Interface** = defines what properties and methods must exist, but not how they work.


## Why use interfaces?

1. **Organize code**: They make your objects and classes follow a clear structure.

2. **Type checking**: TypeScript ensures you follow the correct structure during development.


3. **Reusable code**: You can reuse the same interface for multiple objects or classes.

## Basic syntax of an interface:

```typescript

// interface declaration
interface InterfaceName {
    // properties 
  property1: type;
  property2: type;
 
}
 // using the interface 
class obj implements InterfaceName {
  property1: value1,
  property2: value2
};


```
~~Important:~~ 
- **Every required property in the interface must exist in the class that implements it.**

- **Do you HAVE to use the properties inside the class?**
    No. You only need to declare them, not necessarily use them.


- **The optional properties** can be defined using a question mark `?` after the property name.

```typescript
interface Person {
  name: string;
  age?: number; // optional property
}

let person1: Person = { name: "Sara" }; // valid
let person2: Person = { name: "Noor", age: 30 }; // also valid
``` 

## Implementing an interface in a class:
```typescript
interface Person {
    name: string;
    age: number;
}

class Student implements Person {
    name: string;
    age: number;

    constructor(name: string, age: number) {
        this.name = name;
        this.age = age;
    }
}

const s1 = new Student("Sara", 22);
console.log(s1);
```

## Example Missing a property → Error 
```typescript
interface User {
    id: number;
    username: string;
}

class Admin implements User {
    id: number;
    // username: string;  //  missing → ERROR
}
```

## Example Interface extends another interface
```typescript
interface Product {
    id: number;
    name: string;
}

interface Book extends Product {
    pages: number;
}

class Novel implements Book {
    id: number;
    name: string;
    pages: number;

    constructor(id: number, name: string, pages: number) {
        this.id = id;
        this.name = name;
        this.pages = pages;
    }
}
```

