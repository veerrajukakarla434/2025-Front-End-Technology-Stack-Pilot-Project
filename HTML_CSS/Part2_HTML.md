## HTML Tags & Attributes 

#### Tags

* HTML tags are like keywords which defines that how web browser will format and display the content. With the help of tags, a web browser can distinguish between an HTML content  and a simple content. 
* HTML tags contain three main parts: opening tag, content and closing tag. But some HTML tags are unclosed tags.
* When a web browser reads an HTML document, browser reads it from top to bottom and left to right. HTML tags are used to create HTML documents and render their properties. 
* Each HTML tags have different properties.

#### Attributes 

* HTML attributes are special words which provide additional information about the elements or attributes are the modifier of the HTML element.
* Each element or tag can have attributes, which defines the behaviour of that element.
* Attributes should always be applied with start tag.
* The Attribute should always be applied with its name and value pair.


#### HTML Tags list: Paired and unpaired tags

* The whole HTML functions on HTML Tags. 
* These tags are the basic building block of a website. 

* The types of tags in HTML are categorized on the basis of their appearance. Some tags comes in pairs and others are single. 
   * Paired Tags (Opening and Closing Tags)
   * Unpaired Tags (Singular Tag)

#### Paired Tags - Opening and Closing Tags

* Paired tags are a set of two tags with the same name. In each Paired tag set, one is an opening tag, and the other one is the closing tag. The closing tag has a / slash, it means that the tag is closed now.

* Look at the list of some paired tags in HTML below. Notice that each tag has a closing tag with a slash(/) before the name of the tag.
```java
Syntax: <tag> Content </tag>
```
![image](https://user-images.githubusercontent.com/40323661/151658534-e05607b4-9e38-4039-8d62-4051507b9709.png)

#### Unpaired Tags - Singular Tags

* Unpaired tags are single tags with no closing tag. These tags are also called Singular Tags. These are also called non-container tags because they do not contain any content.

* It is recommended to close the unpaired/singular tags also. But unfortunately, we do not have the closing tag for those. So, an unpaired tag is closed after adding a slash(/) just before the greater than > sign. For example: <br />.

![image](https://user-images.githubusercontent.com/40323661/151658597-900cb0b7-daae-4d86-85a7-df5dcf383c9f.png)

#### HTML <meta> Tag

* **Definition and Usage :**
* The <meta> tag defines metadata about an HTML document. Metadata is data (information) about data.

* <meta> tags always go inside the <head> element, and are typically used to specify character set, page description, keywords, author of the document, and viewport settings.

* Metadata will not be displayed on the page, but is machine parsable.

* Metadata is used by browsers (how to display content or reload page), search engines (keywords), and other web services.

#### HTML Heading Tags - H1 tag to H6 tag

```java
 Heading tag is used to give headings of different sizes in a document. There are six different HTML heading tags, which gives different heading sizes and are defined by <h1> to <h6> tags. <h1> gives the largest heading and <h6> gives the smallest one. So <h1> can be used for most important headings and <h6> can be used for a least important one.
```
  
* **Example**
  
```java
  
<!DOCTYPE html> 
<html lang="en">
   <head>
     <meta charset="UTF-8">
     <title> HTML Heading Tag </title> 
  </head> 

  <body> 
    <h1> This is Heading 1 </h1>
    <h2> This is Heading 2 </h2> 
    <h3> This is Heading 3 </h3> 
    <h4> This is Heading 4 </h4> 
    <h5> This is Heading 5 </h5> 
    <h6> This is Heading 6 </h6> 
  </body> 

</html> 
```


* Tags Refeence : https://www.geeksforgeeks.org/html-tags-complete-reference/
