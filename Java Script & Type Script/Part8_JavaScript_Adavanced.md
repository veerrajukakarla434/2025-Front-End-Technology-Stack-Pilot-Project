## JavaScript Advanced

* JavaScript Set
 * JavaScript Map
* JavaScript RegExp Object
  * JavaScript RegExp
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





