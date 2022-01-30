## HTML & CSS

## HTML Table Borders

 * HTML Table Borders
 * HTML Table Sizes
 * HTML Table Headers
 * HTML Table Padding & Spacing
 * HTML Table Colspan & Rowspan
 * HTML Table Styling
 * HTML Table Colgroup



![image](https://user-images.githubusercontent.com/40323661/151695421-1951b2f8-9aee-4788-8982-f68702e70f50.png)


* HTML tables can have borders of different styles and shapes.


```HTML
<!DOCTYPE html>
<html>
<head>
<style>
	table, th, td {
	  border: 1px solid black;
	}
</style>
</head>
<body>
<h2>Table With Border</h2>
<p>Use the CSS border property to add a border to the table.</p>
<table style="width:100%">
  <tr><th>Firstname</th><th>Lastname</th><th>Age</th></tr>
  <tr><td>Jill</td><td>Smith</td><td>50</td></tr>
  <tr><td>Eve</td><td>Jackson</td><td>94</td></tr>
  <tr><td>John</td><td>Doe</td><td>80</td></tr>
</table>
</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/151695383-e2106e42-944b-462b-b715-987ef86674e7.png)


```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
</style>
</head>
<body>

<h2>Collapsed Borders</h2>
<p>If you want the borders to collapse into one border, add the CSS border-collapse property.</p>

<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
    <td>80</td>
  </tr>
</table>

</body>
</html>
```

![image](https://user-images.githubusercontent.com/40323661/151695470-c3a6bd0f-6750-4569-81d4-c2806d9e0c3e.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid white;
  border-collapse: collapse;
}
th, td {
  background-color: #96D4D4;
}
</style>
</head>
<body>

<h2>Table With Invisible Borders</h2>

<p>Style the table with white borders and a background color of the cells to make the impression of invisible borders.</p>

<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
    <td>80</td>
  </tr>
</table>

</body>
</html>


```
![image](https://user-images.githubusercontent.com/40323661/151695528-54246409-0369-4204-bbe9-dd0959faf9f1.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-radius: 10px;
}
</style>
</head>
<body>

<h2>Table With Rounded Borders</h2>

<p>Use the CSS border-radius property to add rounded corners to the borders.</p>

<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>94</td>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
    <td>80</td>
  </tr>
</table>

</body>
</html>


```
