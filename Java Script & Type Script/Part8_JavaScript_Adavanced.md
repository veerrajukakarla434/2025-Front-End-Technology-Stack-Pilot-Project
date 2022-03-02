

* JavaScript Set
    * Set add() method
    * Set delete() method
    * Set entries() method
    * Set forEach() method
    * Set values() method

 * JavaScript Map
   * Map clear() method
   * Map delete() method
   * Map entries() method
   * Map forEach() method
   * Map get() method
   * Map keys() method
   * Map set() method
   * Map values() method

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

