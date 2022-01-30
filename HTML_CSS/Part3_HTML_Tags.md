## HTML & CSS

## HTML Table Borders

 * HTML Table Borders
 * HTML Table Sizes
 * HTML Table Headers
 * HTML Table Padding & Spacing
 * HTML Table Colspan & Rowspan
 * HTML Table Styling
 * HTML Table Colgroup



## How To Add a Border

* HTML tables can have borders of different styles and shapes.
* When you add a border to a table, you also add borders around each table cell:
* To add a border, use the CSS border property on table, th, and td elements:

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

#### Collapsed Table Borders
* To avoid having double borders like in the example above, set the CSS border-collapse property to collapse.
* This will make the borders collapse into a single border:

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


