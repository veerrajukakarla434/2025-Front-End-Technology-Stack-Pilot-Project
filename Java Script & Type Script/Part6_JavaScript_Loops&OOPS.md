## JavaScript Loops & OOPS

* JavaScript If-else
* JavaScript Switch
* JavaScript Loops
   * for loop
   * while loop
   * do-while loop
   * for-in loop

* JavaScript OOPs
   * JavaScript Class
   * JavaScript Object
   * JavaScript Prototype
   * JavaScript constructor Method
   * JavaScript static Method
   * JavaScript Encapsulation
   * JavaScript Inheritance
   * JavaScript Polymorphism
   * JavaScript Abstraction

#### JavaScript If-else

The **JavaScript if-else statement** is used to execute the code whether condition is true or false. There are three forms of if statement in JavaScript.

  * If Statement
  * If else statement
  * if else if statement

![image](https://user-images.githubusercontent.com/40323661/155841194-b979e831-f595-4148-b39f-c57a2dcd4cc3.png)

```JavaScript
<html>
<body>
<script>  
var a=20;  
if(a>10){  
document.write("value of a is greater than 10");  
}  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/155841226-697e397e-5633-4299-9912-96570e526902.png)


![image](https://user-images.githubusercontent.com/40323661/155841233-ea9e1607-a872-4767-973b-b9a54b05f6ac.png)

```JavaScript

<html>
<body>
<script>  
var a=20;  
if(a%2==0){  
document.write("a is even number");  
}  
else{  
document.write("a is odd number");  
}  
</script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/155841257-7618c9ec-3e98-4501-81fa-6ee5cd95d877.png)

![image](https://user-images.githubusercontent.com/40323661/155841264-1f1282ce-338c-456c-81dc-fa6e5d6395b2.png)

```JavaScript
<html>
<body>
<script>  
var a=20;  
if(a==10){  
document.write("a is equal to 10");  
}  
else if(a==15){  
document.write("a is equal to 15");  
}  
else if(a==20){  
document.write("a is equal to 20");  
}  
else{  
document.write("a is not equal to 10, 15 or 20");  
}  
</script>  
</body>
</html>
```

#### JavaScript Switch

![image](https://user-images.githubusercontent.com/40323661/155841468-7fc530c9-fbc6-4aa6-8146-90a67e2125c8.png)

* **OR**

![image](https://user-images.githubusercontent.com/40323661/155841515-f572d09f-ed89-4328-a158-11e9a1c4c101.png)

![image](https://user-images.githubusercontent.com/40323661/155841536-8d19f9b9-8169-4af0-bb7b-e81b1e441a30.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: switch case</h1>
	
	<script>
		var a = 3;

		switch (a) {
			case 1:
				alert('case 1 executed');
			case 2:
				alert("case 2 executed");
				break;
		   case 3:
				alert("case 3 executed");
				break;
			case 4:
				alert("case 4 executed");
				break;
			default:
				alert("default case executed");
		}

    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/155841563-4124fcb8-e5e7-4a6c-a945-0c4268936081.png)

![image](https://user-images.githubusercontent.com/40323661/155841578-febc27d1-7660-4e49-89d6-c89c21f2714d.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: switch statement</h1>
	
	<script>
		var a = 3;

		switch (a/3) {
			case 1:
				alert("case 1 executed");
				break;
			case 2:
				alert("case 2 executed");
				break;
			case 3:
				alert("case 3 executed");
				break;
			case 4:
				alert("case 4 executed");
				break;
			default:
				alert("default case executed");
		}

    </script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/155841595-46c437f8-47b5-4a15-8964-25ff98fed0ba.png)

![image](https://user-images.githubusercontent.com/40323661/155841604-4494ea3b-eb4c-4d19-9b43-1f31d82d0ac8.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: switch with string type</h1>
	
	<script>
		var str = "bill";

		switch (str) 
		{
			case "steve":
				alert("This is Steve");
			case "bill":
				alert("This is Bill");
				break;
			case "john":
				alert("This is John");
				break;
			default:
				alert("Unknown Person");
				break;
		}
    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/155841674-ca375410-b954-4884-a7ab-b0e7109e3487.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: combined switch cases</h1>
	
	<script>
		var a = 2;

		switch (a) {
			case 1:
			case 2:
			case 3:
				alert("case 1, 2, 3 executed");
				break;
			case 4:
				alert("case 4 executed");
				break;
			default:
				alert("default case executed");
		}
    </script>
</body>
</html>
```

####  JavaScript Loops


![image](https://user-images.githubusercontent.com/40323661/155842113-230f59a6-0ec3-44ea-acb9-5791539170cb.png)

![image](https://user-images.githubusercontent.com/40323661/155842128-4912fe36-6c2a-46a8-bac3-aa936cc8a7f5.png)

![image](https://user-images.githubusercontent.com/40323661/155842140-ac97e0a5-065b-431c-ad46-6ee2077a4b5e.png)


![image](https://user-images.githubusercontent.com/40323661/155842148-66203f74-4db8-426a-a73a-c5967cc3e805.png)


```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript For Loop</h2>

<p id="demo"></p>

<script>
let text = "";

for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}

document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/155842173-0b85f6b1-9e4a-4c70-b179-7b7df98dadbc.png)

![image](https://user-images.githubusercontent.com/40323661/155842222-c1d33baa-4ff6-482c-83c8-abf73bfa8695.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
for (i=1; i<=5; i++)  
{  
document.write(i + "<br/>")  
}  
</script>  
</body>
</html>
```

* **The for loop can also be used to get the values for an array.**

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: for loop</h1>
	<p id="p0"></p>
	<p id="p1"></p>
	<p id="p2"></p>
	<p id="p3"></p>
	<p id="p4"></p>
	
	<script>
		var arr = [10, 11, 12, 13, 14];

		for (var i = 0; i < 5; i++)
		{
			document.getElementById("p" + i).innerHTML = arr[i];
		}

    </script>
</body>
</html>
```

```Javascript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript For Loop</h2>

<p id="demo"></p>

<script>
const cars = ["BMW", "Volvo", "Saab", "Ford", "Fiat", "Audi"];

let text = "";
for (let i = 0; i < cars.length; i++) {
  text += cars[i] + "<br>";
}

document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>

```

#### For/Of and For/In Loops

![image](https://user-images.githubusercontent.com/40323661/155842477-eb8eb244-e80a-42bb-95a0-676e3c136256.png)


![image](https://user-images.githubusercontent.com/40323661/155842493-98c85e30-bf32-4e9e-9835-d3e4f29000de.png)

![image](https://user-images.githubusercontent.com/40323661/155842535-94c6b8d4-a99d-4e23-8173-4fab15278ed3.png)


```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript For In Loop</h2>
<p>The for in statement loops through the properties of an object:</p>

<p id="demo"></p>

<script>
const person = {fname:"John", lname:"Doe", age:25}; 

let txt = "";
for (let x in person) {
  txt += person[x] + " ";
}

document.getElementById("demo").innerHTML = txt;
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/155842637-cbdb96b7-9469-4ff6-ac20-3baae1ec05b8.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript For In</h2>
<p>The for in statement can loops over array values:</p>

<p id="demo"></p>

<script>
const numbers = [45, 4, 9, 16, 25];

let txt = "";
for (let x in numbers) {
  txt += numbers[x] + "<br>"; 
}

document.getElementById("demo").innerHTML = txt;
</script>

</body>
</html>
```






