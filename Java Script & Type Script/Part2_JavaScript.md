## Setup JavaScript Development Environment

* Here, we are going to use JavaScript in developing a web application. So, we must have at least two things, **a browser**, and an **editor** to write the JavaScript code.
* Although we also need a webserver to run a web application, but we will use a single HTML web page to run our JavaScript code. So, no need to install it for now.
![image](https://user-images.githubusercontent.com/40323661/152820583-d428bb30-b6a0-4b1f-a831-6eed7d64ee17.png)


#### IDEs for JavaScript Application Development

* We can write JavaScript code using a simple editor like Notepad. However, you can install any open-sourced or licensed IDE (Integrated Development Environment) to get the advantage of IntelliSense support for JavaScript and syntax error/warning highlighter for rapid development.

![image](https://user-images.githubusercontent.com/40323661/152821026-bfd27c22-735d-4022-9562-650195fc8c33.png)

![image](https://user-images.githubusercontent.com/40323661/152821396-e8821b70-8607-4460-a712-6eae08c0b759.png)

#### Where to write JavaScript & How to write JavaScript

![image](https://user-images.githubusercontent.com/40323661/152825599-6fa084aa-f682-4089-bd00-a9150161a3c6.png)

```HTML
<!DOCTYPE html>
<html>
<head>
</head>
<body>
    <h1> JavaScript Tutorials</h1>
  
    <script>
        //write JavaScript code here..
        alert('Hello, how are you?')
    </script>
</body>
</html>
```
```HTML
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript in Body</h2>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>

</body>
</html> 

```


![image](https://user-images.githubusercontent.com/40323661/152825902-5894a104-d7fe-4289-a0a9-16ceceb186db.png)

![image](https://user-images.githubusercontent.com/40323661/152826101-7dda26db-ba4f-49ad-98c5-c271768744f4.png)

```HTML
<!DOCTYPE html>
<html>
<head>
    <script>
        alert('Executing JavaScript 1')
    </script>
</head>
<body>
    <h1> JavaScript Tutorials</h1>
  
    <script>
        alert('Executing JavaScript 2')
    </script>
    
    <p>This page contains multiple script tags.</p>
    
    <script>
        alert('Executing JavaScript 3')
    </script>
</body>
</html>

```
* Example2
```HTML
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>

<h2>Demo JavaScript in Head</h2>

<p id="demo">A Paragraph.</p>

<button type="button" onclick="myFunction()">Try it</button>

</body>
</html> 
```
* Example3
```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Demo JavaScript in Body</h2>

<p id="demo">A Paragraph.</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>

</body>
</html> 
```
![image](https://user-images.githubusercontent.com/40323661/152826790-acb62fb7-3708-4a44-960d-26d6e38b3b9c.png)

![image](https://user-images.githubusercontent.com/40323661/152826877-3be38e06-c417-462e-9864-d92b65009a58.png)

```HTML
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}

```
```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Demo External JavaScript</h2>

<p id="demo">A Paragraph.</p>

<button type="button" onclick="myFunction()">Try it</button>

<p>This example links to "myScript.js".</p>
<p>(myFunction is stored in "myScript.js")</p>

<script src="myScript.js"></script>

</body>
</html>
```




