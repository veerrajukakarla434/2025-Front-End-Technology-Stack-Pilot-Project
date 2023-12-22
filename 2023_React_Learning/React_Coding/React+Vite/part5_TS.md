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


