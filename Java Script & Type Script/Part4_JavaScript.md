# JavaScript Basics OR JavaScript Fundamentals

* JavaScript Statements
* JavaScript Variables

#### JavaScript Statements

* A computer program is a list of "instructions" to be "executed" by a computer.
* In a programming language, these programming instructions are called statements.
* A JavaScript program is a list of programming statements.
* JavaScript statements are composed of:
    * Values, Operators, Expressions, Keywords, and Comments.
* Most JavaScript programs contain many JavaScript statements.
* The statements are executed, one by one, in the same order as they are written.

 ![image](https://user-images.githubusercontent.com/40323661/153709102-202297a2-e6f9-488a-9b97-6863ab41e47e.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Statements</h2>

<p>A <b>JavaScript program</b> is a list of <b>statements</b> to be executed by a computer.</p>

<p id="demo"></p>

<script>
let x, y, z;  // Statement 1
x = 5;        // Statement 2
y = 6;        // Statement 3
z = x + y;    // Statement 4

document.getElementById("demo").innerHTML =
"The value of z is " + z + ".";  
</script>

</body>
</html>

```

#### JavaScript Variables

* A **JavaScript variable** is simply a name of storage location. There are two types of variables in JavaScript : **local variable** and **global variable**.

![image](https://user-images.githubusercontent.com/40323661/153709261-88a1e8da-ef48-43ea-9369-2a3fcdba4d7f.png)

* **Example** In this example, x, y, and z, are variables, declared with the var keyword:

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Variables</h1>

<p>In this example, x, y, and z are variables.</p>

<p id="demo"></p>

<script>
var x = 5;
var y = 6;
var z = x + y;
document.getElementById("demo").innerHTML =
"The value of z is: " + z;
</script>

</body>
</html>

```

* **Example**  In this example, x, y, and z, are variables, declared with the let keyword:

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Variables</h2>

<p>In this example, x, y, and z are variables.</p>

<p id="demo"></p>

<script>
let x = 5;
let y = 6;
let z = x + y;
document.getElementById("demo").innerHTML =
"The value of z is: " + z;
</script>

</body>
</html>

```

* **Example**  In this example, x, y, and z, are undeclared variables:

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Variables</h1>

<p>In this example, x, y, and z are undeclared variables.</p>

<p id="demo"></p>

<script>
x = 5;
y = 6;
z = x + y;
document.getElementById("demo").innerHTML =
"The value of z is: " + z;
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/153709514-466dbe47-fe69-495b-8f66-24fe6f97b1d2.png)

![image](https://user-images.githubusercontent.com/40323661/153709521-b17d08b6-a2e5-404d-ba30-dd14e3b382ed.png)

![image](https://user-images.githubusercontent.com/40323661/153709545-6f0473c7-decd-45f2-bde2-6a90d0a58a7c.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h1>JavaScript Variables</h1>

<p>In this example, price, price2, and total are variables.</p>

<p id="demo"></p>

<script>
const price1 = 5;
const price2 = 6;
let total = price1 + price2;
document.getElementById("demo").innerHTML =
"The total is: " + total;
</script>

</body>
</html>
```




