## JavaScript Basics OR JavaScript Fundamentals

* Javascript Data Types




#### Javascript Data Types

* JavaScript provides different **data types** to hold different types of values. There are two types of data types in JavaScript.
  * Primitive data type
  * Non-primitive (reference) data type

* JavaScript is a **dynamic type language**, means you don't need to specify type of the variable because it is dynamically used by JavaScript engine. You need to use **var** here to specify the data type. It can hold any type of values such as numbers, strings etc.

* **For example:**

![image](https://user-images.githubusercontent.com/40323661/153751038-5fcddb0a-2d10-4cab-82d1-9ac35e1f69ef.png)

![image](https://user-images.githubusercontent.com/40323661/153751021-2767044b-63d2-4660-b2b5-cfacd0999373.png)


```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Variables </h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	<p id="p3"></p>
	<p id="p4"></p>
	<p id="p5"></p>

	<script>
		var myvariable = 1;  // numeric value
		document.getElementById("p1").textContent = myvariable;

		myvariable = 'one'; // string value
		document.getElementById("p2").textContent = myvariable;

		myvariable = 1.1; // decimal value
		document.getElementById("p3").textContent = myvariable;

		myvariable = true; // Boolean value
		document.getElementById("p4").textContent = myvariable;

		myvariable = null; // null value
		document.getElementById("p5").textContent = myvariable;
    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/153751137-42bc496c-f4ff-4848-bb10-c01cc6326201.png)

* The followings are primitive data types in JavaScript:

![image](https://user-images.githubusercontent.com/40323661/153751242-fced1d55-b7fe-4588-a6a7-c07d0bd3ccae.png)

![image](https://user-images.githubusercontent.com/40323661/153751358-f3e8edd9-1707-4015-84ba-0f57de5c2c62.png)

#### JavaScript String Literals, Objects, Concatenation, Comparison

* The Number is a primitive data type used for positive or negative integer, float, binary, octal, hexadecimal, and exponential values in JavaScript.

* The Number type in JavaScript is double-precision 64 bit binary format like double in C# and Java. It follows the international IEEE 754 standard.

* The first character in a number type must be an integer value, and it must not be enclosed in quotation marks. The following example shows the variables having different types of numbers in JavaScript.


