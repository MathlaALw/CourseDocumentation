# Forms in React


- forms are used to **collect user input**  (such as name, email, password) and handle it in **a controlled and predictable way.**



## Basic Form Example
```jsx
import { useState } from "react";

function LoginForm() {
  const [email, setEmail] = useState("");

  const handleSubmit = (e) => {
    e.preventDefault(); // prevent page reload
    console.log(email);
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="email"
        value={email}
        onChange={(e) => setEmail(e.target.value)}
        placeholder="Enter email"
      />
      <button type="submit">Login</button>
    </form>
  );
}

```

- How It Works : 
    - User types in the input
    - onChange updates the state
    - value comes from state
    - onSubmit runs when the form is submitted


