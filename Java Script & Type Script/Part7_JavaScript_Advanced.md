## JavaScript Advanced :- OOPS (Object-Oriented Programming System)

* JavaScript OOPs
   * JavaScript **Class** 
   * JavaScript **Object**  (We Already Done from previous session)
   * JavaScript **static Method**
   * JavaScript **Abstraction**
   * JavaScript **Inheritance**
   * JavaScript **Polymorphism**
   * JavaScript **Encapsulation**
   *  JavaScript **constructor Method**

 
#### JavaScript Class

![image](https://user-images.githubusercontent.com/40323661/155880173-79d74d25-f328-4d9d-9a1a-692feb55c356.png)

![image](https://user-images.githubusercontent.com/40323661/155880202-65fbb238-044c-441f-9475-f2ec9333504b.png)

![image](https://user-images.githubusercontent.com/40323661/155880219-26ba7b93-2566-424a-916a-78c515aa3fcb.png)

![image](https://user-images.githubusercontent.com/40323661/155881632-1a5b8f11-5a48-4c2c-b845-3f88e0b1153a.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Class</h2>

<p>How to use a JavaScript Class.</p>

<p id="demo"></p>

<script>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
}

const myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML =
myCar.name + " " + myCar.year;
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/155881655-c99c2cb1-fed4-4e68-96eb-57ff5d9c1bc9.png)

![image](https://user-images.githubusercontent.com/40323661/155881660-1160ad24-090d-4190-8a7e-de54955bae7a.png)

![image](https://user-images.githubusercontent.com/40323661/155881678-83ab9f50-65d2-4eb3-9496-38dc7c756045.png)

![image](https://user-images.githubusercontent.com/40323661/155881692-db7ab7a9-69c5-4885-a0ff-883cabfdca62.png)


![image](https://user-images.githubusercontent.com/40323661/155881702-e6552181-f206-4198-9349-81e34a73676e.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Class Method</h2>

<p>How to define and use a Class method.</p>

<p id="demo"></p>

<script>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;

  }
  age() {
    let date = new Date();
    return date.getFullYear() - this.year;
  }
}

let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML =
"My car is " + myCar.age() + " years old.";
</script>

</body>
</html>


```

![image](https://user-images.githubusercontent.com/40323661/155881746-b054f4a9-7807-4569-a7ed-9eb0d97e9d47.png)

```JavaScriprt
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Class Method</h2>

<p>Pass a parameter into the "age()" method.</p>

<p id="demo"></p>

<script>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age(x) {
    return x - this.year;
  }
}

let date = new Date();
let year = date.getFullYear();

let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML=
"My car is " + myCar.age(year) + " years old.";
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/155881766-f30d719d-af6e-4b00-9843-26f7448c2d16.png)

#### JavaScript static Method

* The JavaScript provides static methods that belong to the class instead of an instance of that class. So, an instance is not required to call the static method. These methods are called directly on the class itself.

* **Points to remember**
    * The static keyword is used to declare a static method.
    * The static method can be of any name.
    * A class can contain more than one static method.
    * If we declare more than one static method with a similar name, the JavaScript always invokes the last one.
    * The static method can be used to create utility functions.
    * We can use this keyword to call a static method within another static method.
    * We cannot use this keyword directly to call a static method within the non-static method. In such case, we can call the static method either using the class name or as the property of the constructor.
   
   ![image](https://user-images.githubusercontent.com/40323661/155882049-d47e1ddf-3cc3-4e67-80c0-d5c2cb2ff2b3.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
class Test
{
  static display()
  {
    return "static method is invoked"
  }
}
document.writeln(Test.display());
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/155882067-d0643798-244a-412e-8a16-29f32294102b.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
class Test
{
  static display1()
  {
    return "static method is invoked"
  }
  static display2()
  {
    return "static method is invoked again"
  }
}
document.writeln(Test.display1()+"<br>");
document.writeln(Test.display2());
</script>

</body>
</html>

```
![image](https://user-images.githubusercontent.com/40323661/155882094-294f2875-cc9a-4749-bc21-8299c7c5c66a.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
class Test
{
  static display()
  {
    return "static method is invoked"
  }
  static display()
  {
    return "static method is invoked again"
  }
}
document.writeln(Test.display());
</script>

</body>
</html>

```

![image](https://user-images.githubusercontent.com/40323661/155882169-88b03e19-ff53-4519-8712-87f28f7704c5.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
class Test {
  constructor() {
  document.writeln(Test.display()+"<br>"); 
  document.writeln(this.constructor.display()); 
  }

  static display() {
      return "static method is invoked"
  }
}
var t=new Test();
</script>


</body>
</html>
```
![image](https://user-images.githubusercontent.com/40323661/155882195-1f9c14a6-c5f4-4e49-8970-a1a3134abbbe.png)

```JavaScript
<!DOCTYPE html>
<html>
<body>

<script>
class Test {
  static display() {
      return "static method is invoked"
  }
  
 show() {
  document.writeln(Test.display()+"<br>"); 
  }  
}
var t=new Test();
t.show();
</script>

</body>
</html>
```

