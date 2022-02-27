## JavaScript Advanced :- OOPS (Object-Oriented Programming System)

* JavaScript OOPs
   * JavaScript Class
   * JavaScript Object  (We Already Done from previous session)
   * JavaScript constructor Method
   * JavaScript static Method
   * JavaScript Encapsulation
   * JavaScript Inheritance
   * JavaScript Polymorphism
   * JavaScript Abstraction

 
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


