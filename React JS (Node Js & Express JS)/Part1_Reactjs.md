## Learn React JS with Project

* ES6 Arrow Function

![image](https://user-images.githubusercontent.com/40323661/157073839-77fdadc5-3477-462a-a152-a589dae41caa.png)


![image](https://user-images.githubusercontent.com/40323661/157073545-8d4da653-d5db-4f93-b06e-0c10cbc508a5.png)

## React Fundamentals

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

##  React Router
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

##  React CRUD Axios
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

##  React Search
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

#### ReactJS

* **React is a JavaScript library for building user interfaces.**

* **React is used to build single-page applications.**

* **React allows us to create reusable UI components.**

![image](https://user-images.githubusercontent.com/40323661/157149142-5cd07155-ad3b-43c6-96c3-ade2132c887e.png)

![image](https://user-images.githubusercontent.com/40323661/157149203-5e9fe409-b7b4-4cdc-a98f-de6cc9a82962.png)

![image](https://user-images.githubusercontent.com/40323661/157149338-7fa5b38b-b3e2-49f0-905c-4ebbf4d38a6e.png)

#### React Getting Started

![image](https://user-images.githubusercontent.com/40323661/157149489-a54a9666-c1ea-4147-a6af-4f04b53da9db.png)

![image](https://user-images.githubusercontent.com/40323661/157149626-b73a3f9b-ae91-428e-9619-2879e40fd0ef.png)

![image](https://user-images.githubusercontent.com/40323661/157149682-188ca92e-4546-4c43-9cda-f7ee9f14bafc.png)

```JavaScript
<!DOCTYPE html>
<html>
  <head>
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>

    <div id="mydiv"></div>

    <script type="text/babel">
      function Hello() {
        return <h1>Hello World!</h1>;
      }

      ReactDOM.render(<Hello />, document.getElementById('mydiv'))
    </script>

  </body>
</html>
```

* Refer Below Code Which we will written acual production enviornment 

![image](https://user-images.githubusercontent.com/40323661/157151508-f5081f36-04ec-4c65-9993-590104e115e0.png)

#### Before Creating React Project We Will Learn and Understand React Terminology 

* **React Render HTML**
   * React's goal is in many ways to render HTML in a web page.
   * React renders HTML to the web page by using a function called ReactDOM.render().

![image](https://user-images.githubusercontent.com/40323661/157151979-16af6efa-c6e3-48c4-843b-cc1775cdc1e6.png)


* **React Components**
 * Components are independent and reusable bits of code. They serve the same purpose as JavaScript functions, but work in isolation and return HTML.
 * Components come in two types
     *  Class components and 
     *  Function components
![image](https://user-images.githubusercontent.com/40323661/157152931-21714c1c-bc71-4132-8bd0-1a84b9c47914.png)

![image](https://user-images.githubusercontent.com/40323661/157153036-61816939-3d67-426f-a96a-bd0d4110184b.png)

![image](https://user-images.githubusercontent.com/40323661/157153083-f547631b-e769-4c77-b8e4-724bbd0ac9b9.png)


![image](https://user-images.githubusercontent.com/40323661/157153212-c16596db-71b8-4307-8141-867847938f67.png)


* **React Props**

![image](https://user-images.githubusercontent.com/40323661/157153428-eee22242-300f-47cb-9a85-c81642e41325.png)

* **React State**

![image](https://user-images.githubusercontent.com/40323661/157153875-219cf1b2-cfd3-47e9-ac38-0b0fad58406f.png)

* **React Events**

![image](https://user-images.githubusercontent.com/40323661/157154079-0e01d388-e0bc-4a27-8249-008ab07783c8.png)

* **React Conditional Rendering**

![image](https://user-images.githubusercontent.com/40323661/157154193-ef1b2937-4654-45ce-ac76-b5a761eaf977.png)






