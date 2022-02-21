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



