## Learn React JS with Project

* ES6 Arrow Function

![image](https://user-images.githubusercontent.com/40323661/157073839-77fdadc5-3477-462a-a152-a589dae41caa.png)


![image](https://user-images.githubusercontent.com/40323661/157073545-8d4da653-d5db-4f93-b06e-0c10cbc508a5.png)


* 
* React create-react-app
* React Components
   * Funtional Component
   * Class Component
* JSX
* Props & State
* useState
* useEffect
* React Components
   * LifeCycle
   * Methods
* Conditional Rendering 
* Lists & Keys
* Basic Form Handling


* **----------------React Fundamentals---------------**
  * Intro & Topics to learn in this video
  * Setup
  * Create React App
  * Start React Development Environment 
  * Understand React App Folder Structure
  * Contact App Folder Structure/ Components
  * React "Hello World" Component
  * Adding Sematic UI to Project
  * Understand React Components
  * React JSX
  * Function Component
  * Class Component
  * Rendering List in React
  * Props - Pass data from parent to child
  * Access Props
  * Reference variable in JSX
  * Adding In-line Style
  * Add images in React
  * useState React Hook
  * Pass Function as Prop
  * Update the State using setState()
  * useEffect React Hook

* **------- React Router--------**
  * React Router Intro 
  * Install React Router DOM package
  * Verify installed package
  * Create React Route for application
  * Switch and exact 
  * Passing props in route component
  * Passing props with route render
  * Programmatic navigation with history 
  * Use Link for route
  * Pass data in route state
  * Access route state 
  
* **------- React CRUD Axios--------**
  * Setting up JSON-SERVER
  * Understand Rest API convention
  * Create Contacts Resource
  * Start JSON-SERVER 
  * Install AXIOS package
  * Fetch All Contacts (READ)
  * Add new Contact (CREATE) 
  * Delete a Contact (DELETE)
  * Create an Edit component
  * Edit Contact (UPDATE)

* **------- React Search--------**

  * Adding Search bar JSX
  * Adding useState Hook
  * Add State to Input Element
  * Adding useRef Hook
  * Search Filter with Array Filter Method 
  * Testing & Outro


#### ES6 Arrow Function

* Arrow functions are introduced in ES6, which provides you a more accurate way to write the functions in JavaScript. They allow us to write smaller function syntax. Arrow functions make your code more readable and structured.

![image](https://user-images.githubusercontent.com/40323661/157146397-2c0ac99d-54e1-45fb-aa21-e66ca17808b8.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Arrow Function</h2>

<p>This example shows the syntax of an Arrow Function, and how to use it.</p>

<p id="demo"></p>

<script>
let myFunction = (a, b) => a * b;
document.getElementById("demo").innerHTML = myFunction(4, 5);
</script>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/157146738-d6817dcd-f271-443b-9aea-aede73218978.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Function</h2>

<p>This example shows the syntax of a function, without the use of arrow function syntax.</p>

<p id="demo"></p>

<script>
var hello;

hello = function() {
  return "Hello World!";
}

document.getElementById("demo").innerHTML = hello();
</script>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/157146828-e546e755-de16-47b3-b24a-dfed97844c0b.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Arrow Function</h2>

<p>This example shows the syntax of an Arrow Function, and how to use it.</p>

<p id="demo"></p>

<script>
var hello;

hello = () => {
  return "Hello World!";
}

document.getElementById("demo").innerHTML = hello();
</script>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/157146963-b070c23a-1681-440b-8102-9762944e117f.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Arrow Function</h2>

<p>This example shows an Arrow Function without the brackets or the return keyword.</p>

<p id="demo"></p>

<script>
var hello;

hello = () => "Hello World!";

document.getElementById("demo").innerHTML = hello();
</script>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/157147093-720d9993-3751-49b8-aa8b-a565bfd700f6.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Arrow Function</h2>

<p>This example shows an Arrow Function with a parameter.</p>

<p id="demo"></p>

<script>
var hello;

hello = (val) => "Hello " + val;

document.getElementById("demo").innerHTML = hello("Universe!");
</script>

</body>
</html>
```


