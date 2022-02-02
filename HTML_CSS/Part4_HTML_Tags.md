## HTML , XHTML & CSS

* HTML Comments
* HTML Marquee 
* HTML File Paths & HTML Images
* HTML class Attribute
* HTML id Attribute
* HTML Forms
* HTML Form Attributes
* HTML Form Elements
* HTML Input Types
* HTML Input Attributes
* HTML Input form* Attributes
* HTML Versus XHTML
* HTML JavaScript


#### HTML Comments

![image](https://user-images.githubusercontent.com/40323661/152077039-c6a6ffa2-9676-4d1a-bcd7-12d9e3df4b46.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<!-- This is a comment -->
<p>This is a paragraph.</p>
<!-- Comments are not displayed in the browser -->

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152077138-66be8518-0a9f-4c4a-bb5b-f959a224f7bb.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<p>This is a paragraph.</p>

<!-- <p>This is another paragraph </p> -->

<p>This is a paragraph too.</p>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152077312-b83b61d6-57ce-4a59-8cf9-a4eecbd4fb8e.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<p>This is a paragraph.</p>
<!--
<p>Look at this cool image:</p>
<img border="0" src="pic_trulli.jpg" alt="Trulli">
-->
<p>This is a paragraph too.</p>

</body>
</html>
```
#### HTML Marquee

* The Marquee HTML tag is a non-standard HTML element which is used to scroll a image or text horizontally or vertically.
* In simple words, you can say that it scrolls the image or text up, down, left or right automatically.
* Marquee tag was first introduced in early versions of Microsoft's Internet Explorer. It is compared with Netscape's blink element.

![image](https://user-images.githubusercontent.com/40323661/152077694-ea76d965-751c-4a30-9291-24e2daea713d.png)

```HTML
<!DOCTYPE html>
<html>
<body>
<marquee>This is an example of html marquee </marquee>
</body>
</html>
```
#### HTML File Paths & HTML Images

* A file path describes the location of a file in a web site's folder structure.
![image](https://user-images.githubusercontent.com/40323661/152078271-f97b3b86-88c3-4ee8-8b7a-3ed8b626ef98.png)

![image](https://user-images.githubusercontent.com/40323661/152078314-31683665-e5c7-4f8c-8297-e871748963d7.png)

![image](https://user-images.githubusercontent.com/40323661/152079016-55c6a000-589e-4b00-a02e-a812e1f1f5c5.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Using a Full URL File Path</h2>
<img src="https://www.w3schools.com/images/picture.jpg" alt="Mountain" style="width:300px">

</body>
</html>
```

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Using a Relative File Path</h2>
<img src="C:\Users\veerr\OneDrive\Desktop\2022-2025\images\164101.jpg" alt="Mountain" style="width:300px">

</body>
</html>
```

* Same Folder

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Using a Relative File Path</h2>
<img src="images\164101.jpg" alt="Mountain" style="width:300px">

</body>
</html>
```

* Inside the folder

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Using a Relative File Path</h2>
<img src=".\images\164101.jpg" alt="Mountain" style="width:300px">

</body>
</html>
```

#### HTML class Attribute

![image](https://user-images.githubusercontent.com/40323661/152080820-c6ad6403-db97-4777-8219-e1a137b1c669.png)


![image](https://user-images.githubusercontent.com/40323661/152080063-e9a37aaa-29d5-4632-bb9e-bcf33ff80888.png)


```HTML
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  border: 2px solid black;
  margin: 20px;
  padding: 20px;
}
</style>
</head>
<body>

<div class="city">
<h2>London</h2>
<p>London is the capital of England.</p>
</div> 

<div class="city">
<h2>Paris</h2>
<p>Paris is the capital of France.</p>
</div>

<div class="city">
<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
</div>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152080454-49ca1285-4681-4fd2-bd9c-d5ed4e1bb2e4.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
.note {
  font-size: 120%;
  color: red;
}
</style>
</head>
<body>

<h1>My <span class="note">Important</span> Heading</h1>
<p>This is some <span class="note">important</span> text.</p>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/152080532-b0ae98d9-502e-4bae-b845-02fe2f7f2516.png)


![image](https://user-images.githubusercontent.com/40323661/152080999-1b469136-40a7-4300-8609-77be5824a55e.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
} 

.main {
  text-align: center;
}
</style>
</head>
<body>

<h2>Multiple Classes</h2>
<p>Here, all three h2 elements belongs to the "city" class. In addition, London also belongs to the "main" class, which center-aligns the text.</p>

<h2 class="city main">London</h2>
<h2 class="city">Paris</h2>
<h2 class="city">Tokyo</h2>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/152081044-ac2ff356-6c9d-43f9-817b-d28f539315d7.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
} 
</style>
</head>
<body>

<h2>Different Elements Can Share Same Class</h2>

<p>Even if the two elements do not have the same tag name, they can both point to the same class, and get the same CSS styling:</p>

<h2 class="city">Paris</h2>
<p class="city">Paris is the capital of France.</p>

</body>
</html>
```

#### HTML id Attribute

![image](https://user-images.githubusercontent.com/40323661/152089732-feca0fd0-6550-4abe-8937-68cdea49542e.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
} 
</style>
</head>
<body>

<h2>The id Attribute</h2>
<p>Use CSS to style an element with the id "myHeader":</p>

<h1 id="myHeader">My Header</h1>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/152091999-6c48f716-d314-4803-881a-8705cb999975.png)

#### Difference Between Class and ID

* A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page:

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
/* Style the element with the id "myHeader" */
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}

/* Style all elements with the class name "city" */
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
} 
</style>
</head>
<body>

<h2>Difference Between Class and ID</h2>
<p>A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page:</p>

<!-- An element with a unique id -->
<h1 id="myHeader">My Cities</h1>

<!-- Multiple elements with same class -->
<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152092262-4d5d528b-caa0-428d-9039-1470e9c76335.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<p><a href="#C4">Jump to Chapter 4</a></p>
<p><a href="#C10">Jump to Chapter 10</a></p>

<h2>Chapter 1</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 2</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 3</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C4">Chapter 4</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 5</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 6</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 7</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 8</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 9</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C10">Chapter 10</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 11</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 12</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 13</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 14</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 15</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 16</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 17</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 18</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 19</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 20</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 21</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 22</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 23</h2>
<p>This chapter explains ba bla bla</p>

</body>
</html>
```

#### HTML Forms

* **An HTML form is used to collect user input. The user input is most often sent to a server for processing.**

![image](https://user-images.githubusercontent.com/40323661/152093011-ad6fa6b1-03c4-4adf-ba75-5302e657c61a.png)

![image](https://user-images.githubusercontent.com/40323661/152092639-0bc1d7f8-de0c-49db-98a8-ca0a9e220ae2.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>HTML Forms</h2>

<form action="/backend_acion_class">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 


</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152093186-4b626f91-cbac-45e4-8fae-f36da23c6347.png)

![image](https://user-images.githubusercontent.com/40323661/152093216-34a5e407-69e1-4a50-b3e7-0756fdc3f09a.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Text input fields</h2>

<form>
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe">
</form>

<p>Note that the form itself is not visible.</p>

<p>Also note that the default width of text input fields is 20 characters.</p>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152094177-3ccc94c0-a461-4c65-a1e5-f5bfa11c79df.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Radio Buttons</h2>

<p>Choose your favorite Web language:</p>

<form>
  <input type="radio" id="html" name="fav_language" value="HTML">
  <label for="html">HTML</label><br>
  <input type="radio" id="css" name="fav_language" value="CSS">
  <label for="css">CSS</label><br>
  <input type="radio" id="javascript" name="fav_language" value="JavaScript">
  <label for="javascript">JavaScript</label>
</form> 

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/152094284-cab6424d-8216-4236-915f-2592f74f6743.png)

![image](https://user-images.githubusercontent.com/40323661/152094318-692b6eec-1c04-48f8-a7d8-15c32df6b8c2.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>Checkboxes</h2>
<p>The <strong>input type="checkbox"</strong> defines a checkbox:</p>

<form action="/action_page.php">
  <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
  <label for="vehicle1"> I have a bike</label><br>
  <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
  <label for="vehicle2"> I have a car</label><br>
  <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
  <label for="vehicle3"> I have a boat</label><br><br>
  <input type="submit" value="Submit">
</form> 

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/152094376-c42d7368-fbe6-4c86-9511-b3e31b7e9ff6.png)

![image](https://user-images.githubusercontent.com/40323661/152094407-141fe9c9-ebe4-4fcc-8479-82e17ffafd17.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>HTML Forms</h2>

<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 

<p>If you click the "Submit" button, the form-data will be sent to a page called "/action_page.php".</p>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/152094501-ce3f2de2-31d3-4d55-9540-1cd51151fee8.png)

![image](https://user-images.githubusercontent.com/40323661/152094532-5f9ecfec-f2bf-42c5-a9f3-eae47f94a934.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>The name Attribute</h2>

<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" value="John"><br><br>
  <input type="submit" value="Submit">
</form> 

<p>If you click the "Submit" button, the form-data will be sent to a page called "/action_page.php".</p>

<p>Notice that the value of the "First name" field will not be submitted, because the input element does not have a name attribute.</p>

</body>
</html>

```

#### HTML Form Attributes

![image](https://user-images.githubusercontent.com/40323661/152094800-ccbf193c-c459-4924-9657-54c097f6bffe.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>HTML Forms</h2>

<form action="/action_page.php">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 

<p>If you click the "Submit" button, the form-data will be sent to a page called "/action_page.php".</p>

</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/152095113-50482df8-9501-4c1c-917a-643b0a1d9b0e.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>The form target attribute</h2>

<p>When submitting this form, the result will be opened in a new browser tab:</p>

<form action="/action_page.php" target="_blank">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form> 

</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/152095184-1a6af8f7-a743-48fa-8dc8-ae08be0c49db.png)

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>The method Attribute</h2>

<p>This form will be submitted using the GET method:</p>

<form action="/action_page.php" target="_blank" method="get">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>

<p>After you submit, notice that the form values is visible in the address bar of the new browser tab.</p>

</body>
</html>
```

```HTML
<!DOCTYPE html>
<html>
<body>

<h2>The method Attribute</h2>

<p>This form will be submitted using the POST method:</p>

<form action="/action_page.php" target="_blank" method="post">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value="John"><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="Doe"><br><br>
  <input type="submit" value="Submit">
</form>

<p>After you submit, notice that, unlike the GET method, the form values is NOT visible in the address bar of the new browser tab.</p>

</body>
</html>
```

* **Notes on GET:**

  * Appends the form data to the URL, in name/value pairs
  * NEVER use GET to send sensitive data! (the submitted form data is visible in the URL!)
  * The length of a URL is limited (2048 characters)
  * Useful for form submissions where a user wants to bookmark the result
  * GET is good for non-secure data, like query strings in Google

* **Notes on POST:**

  * Appends the form data inside the body of the HTTP request (the submitted form data is not shown in the URL)
  * POST has no size limitations, and can be used to send large amounts of data.
  * Form submissions with POST cannot be bookmarked










