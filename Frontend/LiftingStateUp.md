# Lifting State Up

## What is Lifting State Up in React?

- **Lifting State Up** is a React concept where you **move state from a child component to a common parent component** so that **multiple components can share and use the same data.**

 - **In Simple Definition**

**Lifting state up** = moving state to the parent so children can communicate through props


## Why do we need Lifting State Up?

- In React:
	- Components can have their own state.
	- but sometimes, multiple components need to share the same state.

- To solve this, we "Lift" the state up to the nearest common parent component.


## Problem without Lifting State Up

```jsx
function ChildA() {
  const [value, setValue] = useState("");
  return <input onChange={e => setValue(e.target.value)} />;
}

function ChildB() {
  return <p>Value shown here</p>;
}
```

- In the above example, `ChildA` has its own state `value`.
- But `ChildB` cannot access that state to display it.
- So, we need to lift the state up to a parent component.

## Solution with Lifting State Up
```jsx

// Parent Component
function Parent() {

// 1. Move state to the Parent
  const [value, setValue] = useState("");
  return (
	<>
	  <ChildA value={value} onChange={setValue} />
	  <ChildB value={value} />
	</>
  );
}


// Child A Component --> pass value and onChange as props
function ChildA({ value, onChange }) {
  return <input value={value} onChange={e => onChange(e.target.value)} />;
}


// Child B Component --> receive value as prop
function ChildB({ value }) {
  return <p>{value}</p>;
}



```