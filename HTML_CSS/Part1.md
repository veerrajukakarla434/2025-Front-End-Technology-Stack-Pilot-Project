## HTML & CSS

* **From This Lesstion What we are going to learn**
   * About HTML OR Introduction
   * What is HTML
   * Advantages & Disadvantages Of HTML
   * Versions  & Browser Supports
   * Building blocks of HTML (Tags and Elements and Attributes)  and its syntax
   * Structure of an HTML Document
   * Editors of HTML to write HTML code and execute 

#### Introduction 
* HTML stands for HyperText Markup Language.
* CSS stands for Cascading Style Sheets.
* HTML is the combination of **Hypertext** and **Markup language**.
* HTML is used to create web pages and web applications.
* We can create a static website by HTML only.
* Technically, HTML is a Markup language rather than a programming language.

#### What is HTML ?
* HTML is an acronym which stands for **Hyper Text Markup Language** which is used for creating web pages and web applications. Let's see what is meant by Hypertext Markup Language, and Web page.

* **Hyper Text**: HyperText simply means "Text within Text." A text has a link within it, is a hypertext. Whenever you click on a link which brings you to a new webpage, you have clicked on a hypertext. HyperText is a way to link two or more web pages (HTML documents) with each other.

* **Markup language**: A markup language is a computer language that is used to apply layout and formatting conventions to a text document. Markup language makes text more interactive and dynamic. It can turn text into images, tables, links, etc.

* **Web Page**: A web page is a document which is commonly written in HTML and translated by a web browser. A web page can be identified by entering an URL. A Web page can be of the static or dynamic type. With the help of HTML only, we can create static web pages.

* HTML was created by Tim **Berners-Lee** in 1991. The first-ever version of HTML was HTML 1.0, but the first standard version was HTML 2.0, published in 1999.

![149184211-16c7f67d-f4e6-4f94-88d6-837794abfdce](https://user-images.githubusercontent.com/50612983/149184211-16c7f67d-f4e6-4f94-88d6-837794abfdce.png "149184211-16c7f67d-f4e6-4f94-88d6-837794abfdce")

#### Advantages:
* HTML is used to build websites.
* It is supported by all browsers.
* It can be integrated with other languages like CSS, JavaScript, etc.

#### Disadvantages:
 * HTML can only create static web pages.
 * For dynamic web pages, other languages have to be used.
 * A large amount of code has to be written to create a simple web page.
 * The security feature is not good.

![](https://user-images.githubusercontent.com/50612983/149185070-75b1c221-c68e-420e-a347-27d1758cb3e8.png "149185070-75b1c221-c68e-420e-a347-27d1758cb3e8")

#### Building blocks of HTML (Tags and Elements and Attributes)
 * An HTML document consist of its basic building blocks which are:
 * **Tags:** 
    * An HTML tag surrounds the content and apply meaning to it. It is written between < and > brackets.
    * HTML tags are like keywords which defines that how web browser will format and display the content. 
    * HTML tags are like keywords which defines that how web browser will format and display the content. 
    * With the help of tags, a web browser can distinguish between an HTML content and a simple content. 
    * HTML tags contain three main parts: opening tag, content and closing tag. 
    * But some HTML tags are unclosed tags.
 

#### Syntax
 ```java
 <tag name  attribute_name= " attr_value"> content </ tag name>   
 ```
 * **Elements:** An HTML element is an individual component of an HTML file. In an HTML file, everything written within tags are termed as HTML elements.
 * An HTML file is made of elements. These elements are responsible for creating web pages and define content in that webpage. 
 * An element in HTML usually consist of a start tag   <tag name>, close tag </tag name> and content inserted between them. 
 * Technically, an element is a collection of start tag, attributes, end tag, content between them.

  ![image](https://user-images.githubusercontent.com/40323661/151218379-de8d8bf8-3d61-40bf-be0d-b3a04224f711.png)

* **Attribute:** An attribute in HTML provides extra information about the element, and it is applied within the start tag. An HTML attribute contains two fields: name & value.
   * HTML attributes are special words which provide additional information about the elements or attributes are the modifier of the HTML element.
   * Each element or tag can have attributes, which defines the behaviour of that element.
   * Attributes should always be applied with start tag.
   * The Attribute should always be applied with its name and value pair.
   * The Attributes name and values are case sensitive, and it is recommended to written in Lowercase only.
   * You can add multiple attributes in one HTML element, but need to give space between two attributes.

#### Structure of an HTML Document
* Elements and Tags: HTML uses predefined tags and elements which tell the browser how to properly display the content.

* If you have used an open tag , then you must use a close tag (except some tags)

* An HTML Document is mainly divided into two parts:

* HEAD: This contains the information about the HTML document. For Example, Title of the page, version of HTML, Meta Data etc.

* BODY: This contains everything you want to display on the Web Page.

* **HTML page structure:** The basic structure of an HTML page is laid out below. 
* It contains the essential building-block elements (i.e. doctype declaration, HTML, head, title, and body elements) upon which all web pages are created.

![](https://user-images.githubusercontent.com/50612983/149246535-feffd293-edd0-48bd-915d-3a4bcf25ee44.png)

```java
<!DOCTYPE html>  
<html>  
  <head>  
    <title>Page Title</title>  
 </head>  
  <body>  
       <h2>Headding Content</h2>  
       <p>Paragraph Content OR paragraph tag</p>  
       <p style="color: red">The style is attribute of paragraph tag</p>  
  </body>  
</html>  

```

#### HTML | Editors

* HTML text editors are used to create and modify web pages. 
* HTML codes can be written in any text editors including the notepad. 
* One just needs to write HTML in any text editor and save the file with an extension “.html”. Some of the popular HTML text editors are given below:

    * Notepad
    * Notepad++
    * Sublime Text 3

