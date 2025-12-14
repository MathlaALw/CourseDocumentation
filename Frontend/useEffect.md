# useEffect Hook in React

## What is useEffect?

The `useEffect` hook in React allows you to perform side effects in function components.
 - Side effects = anything that happens outside rendering the UI.


## Why do we need useEffect?

React components are mainly for rendering UI.
But sometimes you need to:

 - Fetch data from an API

 - Update the document title

 - Set up timers

 - Listen to events

 - Clean up resources


## Basic Syntax
```jsx
import { useEffect } from "react";

useEffect(() => {
  // side effect code here
}, [dependencies]);

```

 - UseEffect takes two arguments:
   1. A function that contains the side effect code. -> () => { // side effect code here }
   2. An optional array of dependencies that determine when the effect should run. ->[dependencies]



## Example 1: Run once on mount
```jsx
useEffect(() => {
  console.log("Component mounted");
}, []);
```
 - Runs only once when the component is rendered for the first time.
 - `[]` = empty dependency array

## Example 2: Run when a value changes
```jsx
import { useState, useEffect } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    console.log("Count changed:", count);
  }, [count]);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```
 - Runs the effect whenever the `count` state changes.
 - `[count]` = dependency array with `count`
 

 ## Example 3: Fetch data from API
 ```jsx
 useEffect(() => {
  fetch("https://jsonplaceholder.typicode.com/users")
    .then(res => res.json())
    .then(data => console.log(data));
}, []);
```
 - Fetches data once when component loads.

 ## Example 4:  Cleanup in useEffect
 ```jsx
 useEffect(() => {
  const timer = setInterval(() => {
    console.log("Running...");
  }, 1000);

  return () => {
    clearInterval(timer);
  };
}, []);

```
 - Sets up a timer when the component mounts. --> mounts -> appears on screen
 - Cleans up the timer when the component unmounts. --> unmounts -> removed from screen


## Summary
- useEffect lets you tell React:
**“After rendering, do this extra work.”** 