## HTML & CSS

## HTML Table Borders

 * HTML Table Borders
 * HTML Table Sizes
 * HTML Table Headers
 * HTML Table Padding & Spacing
 * HTML Table Colspan & Rowspan
 * HTML Table Styling
 * HTML Table Colgroup

* **HTML COLOR PICKER** : https://htmlcolorcodes.com/color-picker/


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
![image](https://user-images.githubusercontent.com/40323661/151695562-01cad78a-a120-4174-94e4-c2afa25a554d.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
th, td {
  border: 1px solid black;
  border-radius: 10px;
}
</style>
</head>
<body>

<h2>Table With Rounded Borders</h2>

<p>Use the CSS border-radius property to add rounded corners to the table cells.</p>

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
![image](https://user-images.githubusercontent.com/40323661/151695607-21046960-024f-4f33-a2bc-9d0dcc4bd70a.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
th, td {
  border-style:solid;
  border-color: #96D4D4;
}
</style>
</head>
<body>

<h2>Table With Border Color</h2>

<p>Use the CSS border-color property to set the color of the borders.</p>

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

#### HTML Table Sizes

![image](https://user-images.githubusercontent.com/40323661/151695812-9fb268f4-803b-4f30-8a56-96f9eb55bb4b.png)

```HTML
<!DOCTYPE html>
<html>
<style>
table, th, td {
  border:1px solid black;
  border-collapse: collapse;
}
</style>

<body>

<h2>100% wide HTML Table</h2>

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
![image](https://user-images.githubusercontent.com/40323661/151695907-704b7400-ff09-4a5b-939c-7384fa84318a.png)

```HTML
<!DOCTYPE html>
<html>
<style>
table, th, td {
  border:1px solid black;
  border-collapse: collapse;
}
</style>
<body>

<h2>Set the first column to 70% of the table width</h2>

<table style="width:100%">
  <tr>
    <th style="width:70%">Firstname</th>
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

![image](https://user-images.githubusercontent.com/40323661/151695935-6bc293a3-a7d9-4665-8b5e-fe5dc8c385c4.png)

```HTML
<!DOCTYPE html>
<html>
<style>
table, th, td {
  border:1px solid black;
  border-collapse: collapse;
}
</style>
<body>

<h2>Set the height of the second row to 200 pixels</h2>

<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <th>Lastname</th> 
    <th>Age</th>
  </tr>
  <tr style="height:200px">
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
#### Table Headers

![image](https://user-images.githubusercontent.com/40323661/151696006-4f592e48-53cb-414b-a75e-e0dad85e4b9c.png)

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

<h2>Table Headers</h2>

<p>Use the TH element to define table headers.</p>

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
</table>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/151696064-6f5fd9be-a93f-46f6-9909-519db7a08a7b.png)

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

<h2>Vertical Table Headers</h2>

<p>The first column becomes table headers if you set the first table cell in each table row to a TH element:</p>

<table style="width:100%">
  <tr>
    <th>Firstname</th>
    <td>Jill</td>
    <td>Eve</td>
  </tr>
  <tr>
    <th>Lastname</th>
    <td>Smith</td>
    <td>Jackson</td>
  </tr>
  <tr>
    <th>Age</th>  
    <td>50</td>
    <td>94</td>
  </tr>
</table>

</body>
</html>


```
![image](https://user-images.githubusercontent.com/40323661/151696096-4253c4cd-e233-496f-988f-ccfaad944290.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th {
  text-align: left;
}
</style>
</head>
<body>

<h2>Left-align Headers</h2>

<p>To left-align the table headers, use the CSS text-align property.</p>

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
</table>

</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/151696132-2dede4a5-72b8-483e-8d72-1e5eeff1279a.png)
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

<h2>A header that spans two columns</h2>

<p>Use the colspan attribute to have a header span over multiple columns.</p>

<table style="width:100%">
  <tr>
    <th colspan="2">Name</th>
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
</table>
</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/151696149-a88e14af-836a-4718-9a70-cc1ef545fd1d.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th, td {
  padding: 5px;
  text-align: left;
}
</style>
</head>
<body>

<h2>Table Caption</h2>
<p>To add a caption to a table, use the caption tag.</p>

<table style="width:100%">
  <caption>Monthly savings</caption>
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
  <tr>
    <td>February</td>
    <td>$50</td>
  </tr>
</table>

</body>
</html>

```

#### HTML Table Padding & Spacing

![image](https://user-images.githubusercontent.com/40323661/151696185-daee6c92-99e9-4401-a78d-70b2d70d105f.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th, td {
  padding: 15px;
}
</style>
</head>
<body>

<h2>Cellpadding</h2>
<p>Cell padding specifies the space between the cell content and its borders.</p>

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

<p><strong>Tip:</strong> Try to change the padding to 5px.</p>

</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/151696242-0976c56f-2b86-4b1c-aabc-f6261b65e9f5.png)

```HTML
<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
th, td {
  padding-top: 10px;
  padding-bottom: 20px;
  padding-left: 30px;
  padding-right: 40px;
}
</style>
</head>
<body>

<h2>Cellpadding - top - bottom - left - right </h2>
<p>We can specify different padding for all fours sides of the cell content.</p>

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

#### HTML Table Colspan & Rowspan
![image](https://user-images.githubusercontent.com/40323661/151696300-8bad3129-f91d-4e4d-a860-f7df8ffb12ae.png)

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

<h2>Cell that spans two columns</h2>
<p>To make a cell span more than one column, use the colspan attribute.</p>

<table style="width:100%">
  <tr>
    <th colspan="2">Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Jill</td>
    <td>Smith</td>
    <td>43</td>
  </tr>
  <tr>
    <td>Eve</td>
    <td>Jackson</td>
    <td>57</td>
  </tr>
</table>
</body>
</html>


```
![image](https://user-images.githubusercontent.com/40323661/151696376-a1c3263e-e123-4b15-88d3-88f2dcb90412.png)

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

<h2>Cell that spans two rows</h2>
<p>To make a cell span more than one row, use the rowspan attribute.</p>

<table style="width:100%">
  <tr>
    <th>Name</th>
    <td>Jill</td>
  </tr>
  <tr>
    <th rowspan="2">Phone</th>
    <td>555-1234</td>
  </tr>
  <tr>
    <td>555-8745</td>
  </tr>
</table>
</body>
</html>

```
#### HTML Table Styling
![image](https://user-images.githubusercontent.com/40323661/151696422-1771b8ed-0e5a-4780-92b7-9120ce632da2.png)
![image](https://user-images.githubusercontent.com/40323661/151696431-18c33301-b70d-4ec5-9938-2f61fe8188ac.png)


