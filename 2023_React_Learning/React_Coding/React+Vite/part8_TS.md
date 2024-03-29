#  State In React, Props V/S State In React

* State is used to store and handle the date between components (Props are only passing the data one component to another component abd which can not store the data, where as State will do that).
* React components has a built-in state object.
* The state object is where you store property values that belong to the component.
* When the state object changes, the component re-renders.

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/b3ae7483-2732-49d9-9db8-4bdab0a8d1a4)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/ee31eb60-05dc-4813-8887-e8a27cb55f51)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/c2e51a2f-294b-47e3-9a59-dc17f925fe19)

* General rule of the state is allways define first statement of the component

* App.tsx
```javascript
import Counter from "./components/Counter";
import Message from "./components/Message";

function App() {
  return (
    <div className="App">
      <Counter />
    </div>
  );
}

export default App;

```

* Counter.tsx
  
```javascript
import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);
  function eventHandle() {
    setCount(count + 1);
  }
  return (
    <div>
      <h1>Count Value is:{count}</h1>
      <button onClick={eventHandle}> Increment</button>
    </div>
  );
}
```
* Output:

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/95ed6474-0c97-4015-bcdb-2037b9a64054)

```javascript
import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);
  function eventHandle() {
    setCount(count + 1);
  }
  function decrementHandle() {
    setCount(count - 1);
  }
  return (
    <div>
      <h1>Count Value is:{count}</h1>
      <button onClick={eventHandle}> Increment</button> <br />
      <button onClick={decrementHandle}> Decrement</button>
    </div>
  );
}
```
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/46273b12-d671-4a06-8029-0d37ebf90f4b)

* **Creating Multiple States In React**

* Here we can increment OR decrement the value by setting and using multiple states
* Counter.tsx
```javascript
import { useState } from "react";

export default function Counter() {
  const [count, setCount] = useState(0);
  const [incrementBy, setIncrementBy] = useState(1);

  function eventHandle() {
    setCount(count + incrementBy);
  }
  function decrementHandle() {
    setCount(count - incrementBy);
  }

  function increaseIncrementBy() {
    setIncrementBy(incrementBy + 1);
  }

  function decrementIncrement() {
    setIncrementBy(incrementBy - 1);
  }

  return (
    <div>
      <h1>Count Value is:{count}</h1>
      <button onClick={eventHandle}> Increment</button>
      <button onClick={decrementHandle}> Decrement</button>
      <h1>We are Increment OR Decrement The value By:{incrementBy}</h1>
      <button onClick={increaseIncrementBy}> Increment</button>
      <button onClick={decrementIncrement}> Decrement</button>
    </div>
  );
}

```  
* Output1 just initial

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/4b8c7531-44f6-4cb4-8c09-a8ad6f9c20f8)

* Count(incremebtby 5) insreasing by 5

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/d55f3327-7885-440d-96f4-b9ae66134711)
