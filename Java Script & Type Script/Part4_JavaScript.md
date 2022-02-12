# JavaScript Basics OR JavaScript Fundamentals

* JavaScript Statements
* JavaScript Variables
   * JavaScript Variable
   * JavaScript local variable
   * JavaScript global variable
* JavaScript Identifiers
* Javascript Operators


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
![image](https://user-images.githubusercontent.com/40323661/153709610-c3c8541c-71b9-4ec3-b22e-6a1a48535994.png)

![image](https://user-images.githubusercontent.com/40323661/153709632-cfa5d529-7a39-4ed8-acf1-cd8a5ad64e3a.png)

![image](https://user-images.githubusercontent.com/40323661/153709661-01af816c-800f-4dd9-9722-a80f398e29af.png)

#### JavaScript local variable

* A JavaScript local variable is declared inside block or function. It is accessible within the function or block only. For example:

![image](https://user-images.githubusercontent.com/40323661/153709745-c6e02bc4-5bdc-434e-b920-b1abad716ef7.png)

#### JavaScript global variable

* A **JavaScript global variable** is accessible from any function. A variable i.e. declared outside the function or declared with window object is known as global variable. 
* For example:

```JavaScript
<html>
<body>
<script>  
var data=200;//gloabal variable  
function a(){  
document.writeln(data);  
}  
function b(){  
document.writeln(data);  
}  
a();//calling JavaScript function
b();
  
</script>  
</body>
</html>

```

#### Javascript Operators

![image](https://user-images.githubusercontent.com/40323661/153710067-af0619a6-758e-441a-8d9e-0d6354feab5d.png)

![image](https://user-images.githubusercontent.com/40323661/153710084-efcd28c9-1bae-474a-b7d2-a81e5451578a.png)

![image](https://user-images.githubusercontent.com/40323661/153710098-e3e7ac8e-e6dd-4184-9212-ed3e318b77e3.png)

* The following example demonstrates how arithmetic operators perform different tasks on operands.

![image](https://user-images.githubusercontent.com/40323661/153710132-95d3e879-ca00-4ff6-9868-f4191fffab74.png)


```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Arithmatic Operators</h1>
	<p>x = 5, y = 10, z;</p>
	<p id="p1">x+y=</p>
	<p id="p2">y-x=</p>
	<p id="p3">x*y=</p>
	<p id="p4">y/x=</p>
	<p id="p5">x%2=</p>
	
	<script>
		var x = 5, y = 10;
		var z = x + y
		document.getElementById("p1").innerHTML += z; //returns 15

		z = y - x;
		document.getElementById("p2").innerHTML += z; //returns 5

		z = x * y;
		document.getElementById("p3").innerHTML += z; //returns 50

		z = y / x;
		document.getElementById("p4").innerHTML += z; //returns 2

		z = x % 2;
		document.getElementById("p5").innerHTML += z; //returns 1
    </script>
</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/153710151-0b350817-6e74-4285-8052-af2f2ebaa957.png)




