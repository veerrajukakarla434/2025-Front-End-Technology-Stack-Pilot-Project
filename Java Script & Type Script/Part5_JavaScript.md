## JavaScript Basics OR JavaScript Fundamentals

* Javascript Data Types
  * String
      * String Object & String String literals 
      * String Methods & Properties
         *  JavaScript String charAt(index) Method
         *  JavaScript String concat(str) Method
         *  JavaScript String indexOf(str) Method
         *  JavaScript String lastIndexOf(str) Method
         *  JavaScript String toLowerCase() Method
         *  JavaScript String toUpperCase() Method
         *  JavaScript String slice(beginIndex, endIndex) Method
         *  JavaScript String trim() Method
         *  JavaScript String split() Method
         *  JavaScript String substring()
  * Number
  * BigInt
  * Boolean
  * Null
  * UnDefined
  * Object
  * Date
  * Array

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

* Here you will learn what string is, how to create, compare and concatenate strings in JavaScript.

* String is a primitive data type in JavaScript. A string is textual content. It must be enclosed in single or double quotation marks.

![image](https://user-images.githubusercontent.com/40323661/153752561-f239d8fc-ccf4-496d-b4c7-209791663fc9.png)

![image](https://user-images.githubusercontent.com/40323661/153752576-0ea0f414-86d7-474f-a1a7-404e09109569.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript String</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	
	<script>
		var str1 = "Hello World";

		var str2 = 'Hello World';

		document.getElementById("p1").innerHTML = str1;
		document.getElementById("p2").innerHTML = str2;
    </script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/153752605-3d98aee6-1f5a-44f9-aa20-8a9bde436790.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript String</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	<p id="p3"></p>
	<p id="p4"></p>
	<p id="p5"></p>
	<p id="p6"></p>
	
	<script>
		var str = 'Hello World';

		document.getElementById("p1").innerHTML = str[0];

		document.getElementById("p2").innerHTML = str[1];

		document.getElementById("p3").innerHTML = str[2];

		document.getElementById("p4").innerHTML = str[3];

		document.getElementById("p5").innerHTML = str[4];

		document.getElementById("p6").innerHTML = str.length

    </script>
</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/153752686-1889763d-74c8-47f8-9267-351cb2f19fa6.png)

![image](https://user-images.githubusercontent.com/40323661/153752704-1fcc77ff-20d0-43d4-8939-33836b87ca5c.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript String</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	
	<script>
		var str = 'Hello World';

		for(var i =0; i< str.length;i++)
		    document.getElementById("p1").innerHTML = document.getElementById("p1").innerHTML + str[i];

		for(var ch of str)
			document.getElementById("p2").innerHTML = document.getElementById("p2").innerHTML + ch;

    </script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/153752753-4e5efb5d-055f-47ad-96d5-58fb6a1991a0.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript String Concatenation</h1>
	
	<p id="p1"></p>
	
	<script>
		var str = 'Hello ' + "World " + 'from ' + 'TutorialsTeacher';

		document.getElementById("p1").innerHTML = str;
    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/153752816-8e6d7ca2-2e7c-44ef-844f-57ea9938de21.png)

![image](https://user-images.githubusercontent.com/40323661/153752826-71c5a83a-0086-4506-8c72-7c1ea8094816.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript String</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	
	<script>
		var str1 = "This is 'simple' string";

		var str2 = 'This is "simple" string';

		document.getElementById("p1").innerHTML = str1;
		document.getElementById("p2").innerHTML = str2;
    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/153753102-a888cd44-405f-4483-9b0b-bd47b9f77fb4.png)

![image](https://user-images.githubusercontent.com/40323661/153753114-6647c049-190c-46f3-b9e1-99b5742bc0c6.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: Quotes in String</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	
	<script>
		var str1 = "This is \"simple\" string";

		var str2 = 'This is \'simple\' string';

		document.getElementById("p1").innerHTML = str1;
		document.getElementById("p2").innerHTML = str2;
    </script>
</body>
</html>
```
#### String object

* Above, we assigned a string literal to a variable. JavaScript allows you to create a String object using the **new** keyword, as shown below.

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript String Object</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	
	<script>
		var str1 = new String();
		str1 = 'Hello World!';

		// or 

		var str2 = new String('Hello World!');

		document.getElementById("p1").innerHTML = str1;
		document.getElementById("p2").innerHTML = str2;
    </script>
</body>
</html>
```
* Be careful while working with String object because comparison of string objects using == operator compares String objects and not the values. 
* Consider the following example.
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: String object comparison</h1>
	
	<p id="p1"></p>
	<p id="p2"></p>
	<p id="p3"></p>
	<p id="p4"></p>
	<p id="p5"></p>
	
	<script>
		var str1 = new String('Hello World');
		var str2 = new String('Hello World');
		var str3 = 'Hello World';
		var str4 = str1;

		document.getElementById("p1").innerHTML = str1 == str2; 
		document.getElementById("p2").innerHTML = str1 == str3; 
		document.getElementById("p3").innerHTML = str1 === str4; 
		document.getElementById("p4").innerHTML = typeof(str1);
		document.getElementById("p5").innerHTML = typeof(str3); 
    </script>
</body>
</html>

![image](https://user-images.githubusercontent.com/40323661/154826361-4c2fde7a-9d97-4eee-a521-8fca54518901.png)

![image](https://user-images.githubusercontent.com/40323661/154826374-c9f2ebe5-dd93-4679-922e-6785f00f9a68.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript String Properties</h2>

<p>The length property returns the length of a string:</p>

<p id="demo"></p>

<script>
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
document.getElementById("demo").innerHTML = text.length;
</script>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154826793-7bddf389-6d38-4e61-ac7e-1942ee151ae7.png)

#### JavaScript String Methods

 * The **JavaScript string** is an object that represents a sequence of characters.
 * String methods help you to work with strings.

![image](https://user-images.githubusercontent.com/40323661/154878895-3eb216af-646f-4d33-a01d-c21fd1007e7c.png)

![image](https://user-images.githubusercontent.com/40323661/154879006-4b3464fd-13e5-4983-9712-312121478ad8.png)


```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
let str="javascript";  
document.write(str.charAt(2));  
</script>  
</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/154879039-7aedf0e1-f46d-4854-ac93-118b3a13a575.png)

![image](https://user-images.githubusercontent.com/40323661/154879076-8d710ae0-238f-4fd4-bf3b-f8447f8ce684.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="javascript ";  
var s2="concat example";  
var s3=s1+s2;  
document.write(s3);  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154879193-58878f60-d4af-4351-a097-301e47136b41.png)

![image](https://user-images.githubusercontent.com/40323661/154879232-2d703eee-a278-4396-b243-4edcf9cc03aa.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="javascript from javatpoint indexof";  
var n=s1.indexOf("i");  
document.write(n);  
</script>  
</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/154879363-60f408b2-cad1-46b1-884f-acf88296759e.png)

![image](https://user-images.githubusercontent.com/40323661/154879380-7421c91c-e1a5-43e8-a567-d0ce90230407.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="javascript from javatpoint indexof";  
var n=s1.lastIndexOf("java");  
document.write(n);  
</script>  
</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/154879544-1cda1444-3b06-46d2-9f87-17a70d124614.png)

![image](https://user-images.githubusercontent.com/40323661/154879580-c867cb2a-df13-4272-a3bb-5705972ee22d.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="JavaScript toLowerCase Example";  
var s2=s1.toLowerCase();  
document.write(s2);  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154879691-56dd2bb6-85c7-4d8e-8b57-93dca3881d1d.png)

![image](https://user-images.githubusercontent.com/40323661/154879733-4ee906d5-16e7-4e63-8593-5cf9efd08411.png)

```Java
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="JavaScript toUpperCase Example";  
var s2=s1.toUpperCase();  
document.write(s2);  
</script>  
</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/154879811-84e7b60a-06fa-4518-a37e-1998312643ff.png)

![image](https://user-images.githubusercontent.com/40323661/154879881-4ef46a14-f22b-408a-843b-7ffd8a64652a.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="abcdefgh";  
var s2=s1.slice(2,5);  
document.write(s2);  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154879957-9e2809ea-f9e8-41e8-8884-04cd6b3c7b32.png)

![image](https://user-images.githubusercontent.com/40323661/154879984-8bf81498-e6b8-468f-a0c0-0f5bc5b28f84.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var s1="     javascript trim    ";  
var s2=s1.trim();  
document.write(s2);  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154880983-976156cf-b45c-4eed-9a17-33c31cc6c576.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>  
var str="This is JavaTpoint website";  
document.write(str.split(" ")); //splits the given string.  
//document.write(str.split(" ", 4)); //splits the given string.  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154881582-4ddabe2d-5aed-4093-9386-14189db781f0.png)

![image](https://user-images.githubusercontent.com/40323661/154881677-9553c864-2e65-4c32-ad71-0223926ed4e3.png)

![image](https://user-images.githubusercontent.com/40323661/154881720-7bce60fe-a729-416f-b282-5e4699a988a3.png)

![image](https://user-images.githubusercontent.com/40323661/154881763-3464ba45-fda4-44ee-8b89-1d218ee5cf4b.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
var str="Javatpoint";
document.writeln(str.substring(0,4));
</script>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154881833-82053933-87d9-494a-ae24-df5d4a3eca8f.png)

![image](https://user-images.githubusercontent.com/40323661/154881865-84d0d891-da26-4c56-84b8-5776efeb715c.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
var str="Javatpoint";
document.writeln(str.substring(5));
</script>

</body>
</html>
```

#### JavaScript Number Object

![image](https://user-images.githubusercontent.com/40323661/154883107-08f6e01e-c3c4-4969-a797-60a2852fc2ac.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<script>
var x=102;//integer value  
var y=102.7;//floating point value  
var z=13e4;//exponent value, output: 130000  
var n=new Number(16);//integer value by number object  
document.write(x+" "+y+" "+z+" "+n);
</script>
</body>
</html>
```

#### ES10 - Bigint type

![image](https://user-images.githubusercontent.com/40323661/154883418-a640fc47-2f3e-4770-a81a-3e519a725d6c.png)


![image](https://user-images.githubusercontent.com/40323661/154883726-ee74823e-e2cb-4d1e-a108-db6961b1a744.png)


```JavaScript
// Parameter in decimal format
var bigNum = BigInt(
"123422222222222222222222222222222222222");
console.log(bigNum);

// Parameter in hexadecimal format
var bigHex = BigInt("0x1ffffffeeeeeeeeef");
console.log(bigHex);

// Parameter in binary format
var bigBin = BigInt(
"0b1010101001010101001111111111111111");
console.log(bigBin);

```

#### JavaScript Boolean

![image](https://user-images.githubusercontent.com/40323661/154969160-a58e442f-6f17-4642-8b3a-cc9265597fde.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Boolean</h1>
	<script>
		var YES = true;
		var NO = false;

		alert(YES);
		alert(NO);
    </script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154969303-e4a23994-82aa-4b2e-9569-122dac09fee9.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Boolean</h1>
	<p id="p1">1 > 2 = </p>
	<p id="p2">a < b = </p>
	<p id="p3">a > b = </p>
	<p id="p4">a + 20 > b + 5 = </p>
	<script>
		var a = 10, b = 20;

		var result = 1 > 2; // false
		document.getElementById("p1").textContent += result;

		result = a < b; // true
		document.getElementById("p2").textContent += result;

		result = a > b; // false
		document.getElementById("p3").textContent += result;

		result = a + 20 > b + 5; // true
		document.getElementById("p4").textContent += result;
	</script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154969508-969601ce-2b4b-4762-8d1c-0544f1241080.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Boolean</h1>
	<p id="p1">Boolean('Hello') returns  </p>
	<p id="p2">Boolean('h') returns  </p>
	<p id="p3">Boolean('10') returns  </p>
	<p id="p4">Boolean([]) returns </p>
	<p id="p5">Boolean(a + b) returns </p>
	
	<script>
		var a = 10, b = 20;

		var b1 = Boolean('Hello'); // true

		var b2 = Boolean('h'); // true

		var b3 = Boolean(10); // true

		var b4 = Boolean([]); // true

		var b5 = Boolean(a + b); // true
		
		document.getElementById("p1").textContent += b1;
		document.getElementById("p2").textContent += b2;
		document.getElementById("p3").textContent += b3;
		document.getElementById("p4").textContent += b4;
		document.getElementById("p5").textContent += b5;
	</script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154969843-2554634c-3870-404d-a268-13b7db4175f1.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Boolean Object</h1>
	<script>
		var bool = new Boolean(true);

		alert(bool); // true
    </script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154970025-e4ceb8e7-3cdf-4338-acd1-0290ca334edf.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Boolean</h1>
	<p id="p1">b1 = </p>
	<p id="p2">b2 = </p>
	<script>
		var b1 = new Boolean(true);
		var b2 = true;

		document.getElementById("p1").textContent += typeof b1;
		document.getElementById("p2").textContent += typeof b2;
	</script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154970499-a9db8702-d9b4-41b9-bcf1-77f3e16e78c9.png)


#### JavaScript Objects

* A javaScript object is an entity having state and behavior (properties and method). For example: car, pen, bike, chair, glass, keyboard, monitor etc.
* JavaScript is an object-based language. Everything is an object in JavaScript.
* JavaScript is template based not class based. Here, we don't create class to get the object. But, we direct create objects.

![image](https://user-images.githubusercontent.com/40323661/154971067-3570c435-b48e-486a-93a2-f69a0f4b1296.png)

![image](https://user-images.githubusercontent.com/40323661/154972221-472ac13a-afcb-4f90-b7cc-4d84bbdfa298.png)

```javaScript
<html>
<body>
<script>  
emp={id:102,name:"Shyam Kumar",salary:40000}  
document.write(emp.id+" "+emp.name+" "+emp.salary);  
</script>
</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/154972371-5e9f5947-0438-4461-8187-d7eb22884ee3.png)

```JavaScript
<html>
<body>
<script>  
var emp=new Object();  
emp.id=101;  
emp.name="Ravi Malik";  
emp.salary=50000;  
document.write(emp.id+" "+emp.name+" "+emp.salary);  
</script> 
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154972709-9081c0a9-bace-46bd-9098-f912c798d4ca.png)
```JavaScript
<html>
<body>
<script>  
function emp(id,name,salary){  
this.id=id;  
this.name=name;  
this.salary=salary;  
}  
e=new emp(103,"Vimal Jaiswal",30000);  
  
document.write(e.id+" "+e.name+" "+e.salary);  
</script>  
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154973956-3c3ba1b2-e3c5-4d4c-9877-140b5fc9b5a8.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Object</h1>
	<p id="p1"></p>
	<p id="p2"></p>
	<p id="p3"></p>
	<p id="p4"></p>
	<p id="p5"></p>
	
	<script>
		var person = { 
                firstName: "James", 
                lastName: "Bond", 
                age: 25, 
                getFullName: function () { 
                    return this.firstName + ' ' + this.lastName 
                    } 
            };

		document.getElementById("p1").innerHTML = person.firstName; 
		document.getElementById("p2").innerHTML = person.lastName; 

		document.getElementById("p3").innerHTML = person["firstName"];
		document.getElementById("p4").innerHTML = person["lastName"];

		document.getElementById("p5").innerHTML = person.getFullName();

    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154974763-729fe80a-4dd9-4414-a631-7f048fd2292d.png)

![image](https://user-images.githubusercontent.com/40323661/154974828-2244dd7d-1b2b-4b65-9607-d62f41d265c9.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Object</h1>
	<p id="p1"></p>
	
	<script>
		var person = new Object();
    
		if(person.hasOwnProperty("firstName")){
          	document.getElementById("p1").textContent = person.firstName;
		}
		else{
        	document.getElementById("p1").textContent = "No firstName property exists";
		}
    </script>
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154974974-85c0944c-4b3b-4645-9c32-89ae62cbdc81.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Nested Object</h1>
	<p id="p1"></p>
	<p id="p2"></p>
	<p id="p3"></p>
	<p id="p4"></p>
	<p id="p5"></p>
	<p id="p6"></p>
	
	<script>
		var p1 = new Object();
		p1.firstName = "James";
		p1.lastName  = "Bond"; 

		var p2 = new Object();

		document.getElementById("p1").textContent = p2.firstName; 
		document.getElementById("p2").textContent = p2.lastName; 
		
		p3 = p1; // assigns object 
		p3.firstName; // James
		p3.lastName; // Bond
		
		document.getElementById("p3").textContent = p3.firstName; 
		document.getElementById("p4").textContent = p3.lastName; 
		
		p3.firstName = "Sachin"; // assigns new value
		p3.lastName = "Tendulkar"; // assigns new value

		document.getElementById("p5").textContent = p3.firstName; 
		document.getElementById("p6").textContent = p3.lastName; 
		
		
    </script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154975388-ca6244d7-c7c5-4d1a-9edc-74586c3a6bb9.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
	<h1>Demo: JavaScript Object using for-in Loop</h1>
	
	<script>
		var person = new Object();
		person.firstName = "James";
		person.lastName = "Bond";

		for(var prop in person){
				alert(prop);  // access property name
				alert(person[prop]); // access property value
			};

    </script>
</body>
</html>
```

#### JavaScript Date Object

![image](https://user-images.githubusercontent.com/40323661/154976479-5bd21208-380d-49fd-8e07-82c398d47343.png)

![image](https://user-images.githubusercontent.com/40323661/154976674-df12eea6-f8cb-47da-963b-2436df19c4be.png)

```JavaScript
<html>
<body>
Current Date and Time: <span id="txt"></span>  
<script>  
var today=new Date();  
document.getElementById('txt').innerHTML=today;  
</script>  
</body>
</html>

===========================================================
Let's see another code to print date/month/year.

<script>  
var date=new Date();  
var day=date.getDate();  
var month=date.getMonth()+1;  
var year=date.getFullYear();  
document.write("<br>Date is: "+day+"/"+month+"/"+year);  
</script> 
=========================================================

```
![image](https://user-images.githubusercontent.com/40323661/154976999-5e687d07-c399-4f2d-82a6-87f44290ecf6.png)

```JavaScript
<html>
<body>
Current Time: <span id="txt"></span>
<script>
var today=new Date();
var h=today.getHours();
var m=today.getMinutes();
var s=today.getSeconds();
document.getElementById('txt').innerHTML=h+":"+m+":"+s;
</script>
</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/154977282-325b4551-450a-456d-ad31-51d1c8c3f1af.png)

```JavaScript
<html>
<body>
Current Time: <span id="txt"></span>  
<script>  
window.onload=function(){getTime();}
function getTime(){  
var today=new Date();  
var h=today.getHours();  
var m=today.getMinutes();  
var s=today.getSeconds();  
// add a zero in front of numbers<10  
m=checkTime(m);  
s=checkTime(s);  
document.getElementById('txt').innerHTML=h+":"+m+":"+s;  
setTimeout(function(){getTime()},1000);  
}  
//setInterval("getTime()",1000);//another way  
function checkTime(i){  
if (i<10){  
  i="0" + i;  
 }  
return i;  
}  
</script>  
</body>
</html>

```

#### JavaScript Array
![image](https://user-images.githubusercontent.com/40323661/154977802-ecca2b17-cba6-4378-ad0e-a9e8e3395140.png)

![image](https://user-images.githubusercontent.com/40323661/154977852-8aed01ec-c1fb-4621-ae9d-97c657d34734.png)


```JavaScript
<html>
<body>
<script>  
var emp=["Sonoo","Vimal","Ratan"];  
for (i=0;i<emp.length;i++){  
document.write(emp[i] + "<br/>");  
}  
</script>  
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154978335-bdc11a0a-54e6-44e6-a818-4be0af099228.png)

![image](https://user-images.githubusercontent.com/40323661/154978392-1fe788f8-3f52-456c-b481-a2802c1d5b53.png)

```JavaScript
<html>
<body>
<script>  
var i;  
var emp = new Array();  
emp[0] = "Arun";  
emp[1] = "Varun";  
emp[2] = "John";  
  
for (i=0;i<emp.length;i++){  
document.write(emp[i] + "<br>");  
}  
</script>  
</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/154978553-193d2bf8-2a67-4014-83b0-4f5c7d7b186d.png)

```JavaScript
<html>
<body>
<script>  
var emp=new Array("Jai","Vijay","Smith");  
for (i=0;i<emp.length;i++){  
document.write(emp[i] + "<br>");  
}  
</script>  
</body>
</html>
```


