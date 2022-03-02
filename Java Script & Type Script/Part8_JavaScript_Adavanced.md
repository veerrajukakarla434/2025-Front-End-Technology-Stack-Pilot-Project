## JavaScript Advanced

* JavaScript Set
 * JavaScript Map
* JavaScript JSON Object
   * JavaScript JSON
   * JSON.parse() method
   * JSON.stringify() method


#### JavaScript Set Object

* The JavaScript Set object is used to store the elements with unique values. The values can be of any type i.e. whether primitive values or object references.

![image](https://user-images.githubusercontent.com/40323661/156365970-18c93b36-6121-4cf2-9f13-a99e44856f49.png)

![image](https://user-images.githubusercontent.com/40323661/156366029-5201fbb7-0e37-42a2-aaf1-405cbb22bdf2.png)

![image](https://user-images.githubusercontent.com/40323661/156366197-f7aefda9-ff1e-4d2d-b3b5-84b021df5e81.png)

![image](https://user-images.githubusercontent.com/40323661/156366233-ce940330-3781-4d90-aa35-66ad561d90ed.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Sets</h2>
<p>Create a Set from an Array:</p>

<p id="demo"></p>

<script>
// Create a Set
const letters = new Set(["a","b","c"]);

// Display set.size
document.getElementById("demo").innerHTML = letters.size;
</script>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/156366358-cf8be16c-1ad3-41de-b4e0-34a8932de0fb.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Sets</h2>
<p>Add values to a Set:</p>

<p id="demo"></p>

<script>
// Create a Set
const letters = new Set();

// Add Values to the Set
letters.add("a");
letters.add("b");
letters.add("c");

// Display set.size
document.getElementById("demo").innerHTML = letters.size;
</script>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/156366470-21f33e4f-1dff-438c-9bf5-34bd69fa06ec.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Sets</h2>
<p>forEach() calls a function for each element:</p>

<p id="demo"></p>

<script>
// Create a Set
const letters = new Set(["a","b","c"]);

// List all Elements
let text = "";
letters.forEach (function(value) {
  text += value + "<br>";
})

document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/156366682-c9c0e03b-2042-4ed6-bb90-ccf804913580.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Sets</h2>
<p>Set.values() returns a Set Iterator:</p>

<p id="demo"></p>

<script>
// Create a Set
const letters = new Set(["a","b","c"]);

// Display set.size
document.getElementById("demo").innerHTML = letters.values();
</script>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/156366809-89b80d7d-613f-4aac-920e-61a7d4251cfd.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Sets</h2>
<p>Iterating Set values:</p>

<p id="demo"></p>

<script>
// Create a Set
const letters = new Set(["a","b","c"]);

// List all Elements
let text = "";
for (const x of letters.values()) {
  text += x + "<br>";
}

document.getElementById("demo").innerHTML = text;
</script>
</body>
</html>

```
#### JavaScript Maps

![image](https://user-images.githubusercontent.com/40323661/156367344-2a59c672-57fa-45c0-ac5e-cbf7c36698d1.png)


![image](https://user-images.githubusercontent.com/40323661/156367382-5b9d3c51-93fa-4156-8ba0-731c23353762.png)


![image](https://user-images.githubusercontent.com/40323661/156367428-6d027d05-ede8-4958-80f0-2ce8f78de23e.png)


```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Map Objects</h2>
<p>Creating a Map from an Array:</p>

<p id="demo"></p>

<script>
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);

document.getElementById("demo").innerHTML = fruits.get("apples");
</script>

</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/156367536-120f1f49-2abe-4894-9021-44ff76510c83.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Map Objects</h2>
<p>Using Map.set():</p>

<p id="demo"></p>

<script>
// Create a Map
const fruits = new Map();

// Set Map Values
fruits.set("apples", 500);
fruits.set("bananas", 300);
fruits.set("oranges", 200);

document.getElementById("demo").innerHTML = fruits.get("apples");
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/156368042-2d5353d1-cbc0-4b40-8a9e-766dc80c3c8c.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>
<h2>JavaScript Maps</h2>
<p>Deleting Map elements:</p>

<p id="demo"></p>

<script>
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);

// Delete an Element
fruits.delete("apples");

document.getElementById("demo").innerHTML = fruits.size;
</script>

</body>
</html>

```

#### JSON - Introduction

![image](https://user-images.githubusercontent.com/40323661/156368903-c9b69673-9535-4ad2-abad-1ffb90b94721.png)

![image](https://user-images.githubusercontent.com/40323661/156369102-2282ab34-b289-4c70-afd4-231fcd422d30.png)

![image](https://user-images.githubusercontent.com/40323661/156369146-928b91b1-c3b7-4589-88dc-3f9312faff48.png)

![image](https://user-images.githubusercontent.com/40323661/156369202-5c4df476-5e7d-4d5d-a012-12a03426df46.png)

![image](https://user-images.githubusercontent.com/40323661/156369472-e9c540ac-643f-4b7d-93d6-730772619870.png)

#### JSON.parse()

![image](https://user-images.githubusercontent.com/40323661/156369694-8bbfa13b-46df-4b4e-9386-2875762fa94d.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>Creating an Object from a JSON String</h2>

<p id="demo"></p>

<script>
const txt = '{"name":"John", "age":30, "city":"New York"}'
const obj = JSON.parse(txt);
document.getElementById("demo").innerHTML = obj.name + ", " + obj.age;
</script>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/156369819-e4ef3e02-fb51-4fa7-890d-d224aa3bdbdf.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>Parsing a JSON Array.</h2>
<p>Data written as an JSON array will be parsed into a JavaScript array.</p>
<p id="demo"></p>

<script>
const text = '[ "Ford", "BMW", "Audi", "Fiat" ]';
const myArr = JSON.parse(text);
document.getElementById("demo").innerHTML = myArr[0];
</script>

</body>
</html>
```
#### JSON.stringify()

![image](https://user-images.githubusercontent.com/40323661/156370380-e8c31c02-d476-4f59-8b7b-199a29cb74de.png)

![image](https://user-images.githubusercontent.com/40323661/156370462-32e018ce-e195-4fc4-9c5d-b6ade6dc3d0f.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>Create a JSON string from a JavaScript object.</h2>
<p id="demo"></p>

<script>
const obj = {name: "John", age: 30, city: "New York"};
const myJSON = JSON.stringify(obj);
document.getElementById("demo").innerHTML = myJSON;
</script>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/156370566-f28b90f0-8593-4d47-a880-bf7f8ee9cd42.png)

![image](https://user-images.githubusercontent.com/40323661/156370601-e821b023-aad2-43d9-bf01-72d2a8147f44.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>Create a JSON string from a JavaScript array.</h2>
<p id="demo"></p>

<script>
const arr = ["John", "Peter", "Sally", "Jane"];
const myJSON = JSON.stringify(arr);
document.getElementById("demo").innerHTML = myJSON;
</script>

</body>
</html>
```




