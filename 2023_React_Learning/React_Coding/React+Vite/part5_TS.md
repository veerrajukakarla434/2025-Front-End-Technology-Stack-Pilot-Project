# React Props

* We can make components more dynamic using props.
* Props are arguments passed into React components.
* Props are passed to components via **HTML attributes**.
* **props stands for properties**.

* **Example:**
* * Hello.tsx
```java
function Hello(props) {
  return (
    <div>
      <h1>Hello {props.name}</h1>
    </div>
  );
}
export default Hello;
```
* App.tsx
```java
import Hello from "./components/Hello";

function App() {
  return (
    <div className="App">
      <Hello name="Veer" />
    </div>
  );
}

export default App;
```
* Output:
  
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/a6681c00-e3e0-4f9d-bed2-15f5697de513)

* We can send 100% dynamic

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/775c6375-32ea-460b-b257-a66a7a456aac)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/1a50c58e-66bd-4ca6-9fc9-9804c4982cf1)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/8458762e-c562-4b3c-8bcc-6520afa8d91f)
  
#### Destructuring of Props in ReactJS

* **What is destructuring?**

* **Destructuring** was introduced in ES6. It’s a JavaScript feature that allows us to extract multiple pieces of data from an array or object and assign them to their own variables.

* Imagine you have a person object with the following properties:
```java
const person = {
  firstName: "Lindsay",
  lastName: "Criswell",
  city: "NYC"
}
```
* Destructuring is a simple property that is used to make code much clear and readable, mainly when we pass props in React.

* **What is Destructuring?**

* Destructuring is a characteristic of JavaScript, It is used to take out sections of data from an array or objects, We can assign them to new own variables created by the developer.
* In destructuring, It does not change an array or any object, it makes a copy of the desired object or array element by assigning them in its own new variables, later we can use this new variable in React (class or functional) components.
* It makes the code more clear. When we access the props using this keyword, we have to use this/ this.props throughout the program, but by the use of restructuring, we can discard this/ this.props by assigning them in new variables.
* This is very difficult to monitor props in complex applications, so by assigning these props in new own variables we can make a code more readable.

* Hello.tsx
```java
function Hello(props) {
  const { name, message } = props;
  return (
    <div>
      <h1>
        {name} {message}
      </h1>
    </div>
  );
}
export default Hello;

```
* App.tsx

```java
import Hello from "./components/Hello";

function App() {
  return (
    <div className="App">
      <Hello name="Veer" message="How are you" />
    </div>
  );
}

export default App;

```
* main.tsx
```java
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import Hello from "./components/Hello";

ReactDOM.createRoot(document.getElementById("root") as HTMLElement).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);

```
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/af3c9637-b031-4064-bb18-f02df33bca06)

* We can destructuring the props like below
```java
  function Hello(name, message) {
  return (
    <div>
      <h1>
        {name} {message}
      </h1>
    </div>
  );
}
export default Hello;
```

####  Immutability of Props

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/536ec38b-8686-49ff-bb75-1238c9cc5935)

* Props are immutable, If you try to change name which has passed throug pops you will get bellow error

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/824673bc-7ba0-4489-8f66-119f7c1aa748)
  
#### Passing Arrays, Ojects via Props
* Hello.tsx
```java
function Hello(props) {
  return (
    <div>
      <h1>
        {props.name} {props.message} {props.seatNumbers}
      </h1>
    </div>
  );
}
export default Hello;
```
* App.tsx
```java
import Hello from "./components/Hello";

function App() {
  const seatNumbers = [1, 2, 3, 5];
  return (
    <div className="App">
      <Hello name="Veer" message="How are you" seatNumbers={seatNumbers} />
    </div>
  );
}

export default App;
```
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/63999fa5-5aa2-4572-96f7-1139c3720205)

* **Listing the arrary objects using map**
```javascript
export default function Fruits() {
  const fruits = ["Apple", "Banana", "Orange", "Mango", "Pineapple"];
  return (
    <div>
      {fruits.map((fruit) => (
        <h1>{fruit}</h1>
      ))}
    </div>
  );
}

```
```javascript
import Fruits from "./components/Fruits";

function App() {
  return (
    <div className="App">
      <Fruits />
    </div>
  );
}

export default App;
```
* Output
 
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/bda3fceb-99ab-40f6-9166-0502d4a3ea3f)

* We can go for list of object by using or adding **li** and **UL**
  
```javascript
export default function Fruits() {
  const fruits = ["Apple", "Banana", "Orange", "Mango", "Pineapple"];
  return (
    <div>
      <ul>
        {fruits.map((fruit) => (
          <li>{fruit}</li>
        ))}
      </ul>
    </div>
  );
}

```
* Output will be

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/762ace4a-6d34-4cd2-bc5b-5b5e87332eff)

* Still we are getting some error becuase of array object or value should have key (refer below code)

```javascript
export default function Fruits() {
  const fruits = ["Apple", "Banana", "Orange", "Mango", "Pineapple"];
  return (
    <div>
      <ul>
        {fruits.map((fruit) => (
          <li key={fruit}>{fruit}</li>
        ))}
      </ul>
    </div>
  );
}
```  
* Above object is having only single array ogbject, now we can see complex object rendering
```javascript
export default function Fruits() {
  //const fruits = ["Apple", "Banana", "Orange", "Mango", "Pineapple"];

  const fruits = [
    { name: "Apple", price: 10, color: "red" },
    { name: "Banana", price: 5, color: "yellow" },
    { name: "Orange", price: 8, color: "Orange" },
    { name: "Mango", price: 15, color: "yellow" },
    { name: "Pineapple", price: 30, color: "yellow" },
  ];

  return (
    <div>
      <ul>
        {fruits.map((fruit) => (
          <li key={fruit.name}>
            {" "}
            {fruit.name} ${fruit.price} {fruit.color}{" "}
          </li>
        ))}
      </ul>
    </div>
  );
}

```
* Output
  
 ![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/568b84b5-f026-4abb-9b22-3c0befb2746f)
     
#### Props: Rendering Components Inside A Loop

* App.tx
```javascript
import Fruits from "./components/Fruits";

function App() {
  return (
    <div className="App">
      <Fruits />
    </div>
  );
}

export default App;
```
* Fruits.tsx
```java
import Fruit from "./Fruit";

export default function Fruits() {
  //const fruits = ["Apple", "Banana", "Orange", "Mango", "Pineapple"];

  const fruits = [
    { name: "Apple", price: 10, color: "red" },
    { name: "Banana", price: 5, color: "yellow" },
    { name: "Orange", price: 8, color: "Orange" },
    { name: "Mango", price: 15, color: "yellow" },
    { name: "Pineapple", price: 30, color: "yellow" },
  ];

  return (
    <div>
      <ul>
        {fruits.map((fruit) => (
          <Fruit
            key={fruit.name}
            name={fruit.name}
            price={fruit.price}
            color={fruit.color}
          />
        ))}
      </ul>
    </div>
  );
}
```
* Fruit.tsx
```javascript
export default function Fruit({ name, price, color }: any) {
  return (
    <li key={name}>
      {name} ${price} {color}
    </li>
  );
}
```
  
