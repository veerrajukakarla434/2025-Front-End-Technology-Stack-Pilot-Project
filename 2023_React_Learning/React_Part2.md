# 2023 React Learning

#### ReactJS Class Components

* **Class components in React :**
* React **class components** are the bread and butter of most modern web apps built in ReactJS. These components are simple classes (made up of multiple functions that add functionality to the application). All **class components** are child classes for the Component class of ReactJS.

* **Creating class Components**
* We will learn how to create class components with the help of an example

* **Example:** Program to demonstrate the creation of class components. Create a React app and edit the **App.js** as:

* **Filename- App.js:**

```java
import React from "react"; 

class App extends React.Component { 
render() { 
	return <h1>GeeksForGeeks</h1>; 
} 
} 

export default App;
```
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/94490bfc-4ecd-4bae-b0e7-0e7f4e4f09ee)

* Example: Open the App.js file and replace the code with the below code.

```java
import React from "react"; 

class Sample extends React.Component { 
render() { 
	return <h1>A Computer Science Portal For Geeks</h1>; 
} 
} 

class App extends React.Component { 
render() { 
	return <Sample />; 
} 
} 

export default App;

```
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/8f3fb0ae-1d03-408f-be69-7bdf8375f2f3)

* **Advantages of class Components over Functional Components**

* The main feature of **class components** that distinguished them from functional components is that they have access to a **state** which dictates the current behavior and appearance of the component (Later, with React Hooks introduced in version 16.8, we are able to declare a stateful component without declaring a class). This **state** can be modified by calling the **setState() function**. One or more variables, arrays, or objects defined as part of the state can be modified at a time with the **setState()function**.

* For More Reference -> https://www.geeksforgeeks.org/reactjs-class-components/

#### ReactJS Functional Components

* **ReactJS Functional components** are some of the more common components that will come across while working in React. These are simply JavaScript functions. We can create a functional component in React by writing a JavaScript function. These functions may or may not receive data as parameters. In the functional Components, the return value is the JSX code to render to the DOM tree.

* **Ways to call the functional component:**

* We can call the functions in javascript in other ways as follows:

* **1. Call the function by using the name of the function followed by the Parentheses.**
```java
// Example of Calling the function with function name followed by Parentheses
import React from 'react';
import ReactDOM from 'react-dom/client';
function Parentheses() {
    return (<h1>
                We can call function using name of the 
                function followed by Parentheses 
            </h1>);
}
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(Parentheses());
```
* **2. Call the function by using the functional component method.**

```java
// Example of Calling the function using component call
import React from 'react';
import ReactDOM from 'react-dom/client';
function Comp() {
    return (<h1> As usual we can call the function using component call</h1>);
}
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Comp />);
```
* Now, We will use the functional component method to create a program and see how functional components render the component in the browser.
* **Program to demonstrate the creation of functional components**
* Open your React project directory and go to the src folder then edit the index.js file.

```java
//index.js File 
import React from 'react'; 
import ReactDOM from 'react-dom'; 
import Demo from './App'; 

ReactDOM.render( 
	<React.StrictMode> 
		<Demo /> 
	</React.StrictMode>, 
	document.getElementById('root') 
);
```
* Open the App.js file from the src folder and edit the file.
```java
//App.js File 
import React from 'react'; 
import ReactDOM from 'react-dom'; 

const Demo=()=>{return <h1>Welcome to GeeksforGeeks</h1>}; 
export default Demo;
```

* **Problem with using functional components**
* **Functional components** lack a significant amount of features as compared to class-based components and they do not have access to dedicated state variables like **class-based components.**

* **Advantage of using hooks in functional components**
The problem discussed above is solved with the help of a special ReactJS concept called “hooks”. ReactJS has access to a special hook called **useState().** The **useState()** is used to initialize only one state variable to multiple state variables. The first value returned is the initial value of the state variable, while the second value returned is a reference to the function that updates it.

 * For more info -> https://www.geeksforgeeks.org/reactjs-functional-components/

* **ReactJS Lifecycle of Components**
* Ref -> https://www.geeksforgeeks.org/reactjs-lifecycle-components/?ref=lbp

* **Differences between Functional Components and Class Components**
* Ref-> https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components/?ref=lbp

#### ReactJS Props & State

* **ReactJS Methods as Props**
* **What are props?**
* We know that everything in ReactJS is a component and to pass in data to these components, props are used. Whenever we call child components from parents we can pass data as props. This helps the parent component communicate with the child.

Although passing in props like this is great, it surely lacks flexibility in an application. For example, we cannot let the child communicate with the parent in this way. This, nonetheless, can be done by passing methods as props in ReactJS. 


* Props are arguments passed into React components.
* Props are passed to components via HTML attributes.
* React Props are like function arguments in JavaScript and attributes in HTML.
* To send props into a component, use the same syntax as HTML attributes:

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/cb50923e-d791-4c99-a779-58c11b1cd8f3)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/0302a5df-30b7-40bd-b13f-253b5cf2e26c)



