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









