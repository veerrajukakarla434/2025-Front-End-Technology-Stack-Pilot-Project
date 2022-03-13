## ReactJS  React Fundamentals

#### Function & Class Components

* Class Component Example
```javaScript
import React, { Component } from 'react'

export default class App extends Component {
  render() {
    return (
     
      <div>
        <h2>Welcome to React JS CLass Component Example</h2>
      </div>
      
    )
  }
}

```

![image](https://user-images.githubusercontent.com/40323661/157407526-ee8ea422-447a-481e-98de-020b8d99099d.png)

![image](https://user-images.githubusercontent.com/40323661/157407586-c9fe5146-8f79-449d-bfd1-fb53c0315345.png)

#### State in Class Component in ReactJs 
* Here we can store / take valuse from **state**  (state management feauture from class component)

![image](https://user-images.githubusercontent.com/40323661/157408624-7820b976-7cc7-4f10-a985-fb093122d15e.png)

![image](https://user-images.githubusercontent.com/40323661/157408678-0eb98962-30b5-4fae-8577-18a36299f40b.png)

####  Props in Class Component in ReactJs 

* Properties are nothing but send properties one class to another class

![image](https://user-images.githubusercontent.com/40323661/157704637-7e70ce3e-397a-4753-9593-32c72ead39e6.png)

![image](https://user-images.githubusercontent.com/40323661/157704776-5c54f9c4-c186-4bd1-92be-ad2678b115a5.png)

![image](https://user-images.githubusercontent.com/40323661/157704867-94e68216-38b8-40a1-bb7f-61042933c8b2.png)

#### How to Use CSS Styling in ReactJs 

![image](https://user-images.githubusercontent.com/40323661/157709270-1eee33d5-d3d8-4217-8b63-2464f8e8db81.png)

![image](https://user-images.githubusercontent.com/40323661/157709524-bf0136f6-ccf9-4f1b-b104-8b908b5cf434.png)


![image](https://user-images.githubusercontent.com/40323661/157709446-3f7d95d4-e2e0-4ae4-ae3b-9a2837a7a6d6.png)


* Now Using Funtional React Component 

![image](https://user-images.githubusercontent.com/40323661/157409159-0000d803-3e0b-4f60-96f9-bd15f4ac948c.png)

![image](https://user-images.githubusercontent.com/40323661/157409202-b2579cf2-7fb9-42e7-a3d7-509cbed3ea8c.png)

![image](https://user-images.githubusercontent.com/40323661/157411707-d7c76098-9460-45bf-b5bb-02bda34d0424.png)

![image](https://user-images.githubusercontent.com/40323661/157414585-2364940c-f150-4574-aab5-44d900de066e.png)

![image](https://user-images.githubusercontent.com/40323661/157414710-5c6ebf24-a61d-4a89-8557-852e9c6ef712.png)

![image](https://user-images.githubusercontent.com/40323661/157412974-4609ce59-780c-43a4-bfce-9347e3419571.png)

![image](https://user-images.githubusercontent.com/40323661/157413017-d7f627d9-8f2c-4e77-a986-dd28b34f1e99.png)

* onClick in ReactJs   (we can see result in console from browser)

![image](https://user-images.githubusercontent.com/40323661/157712767-9aec9527-949e-4d42-9d6f-23ad527fac1b.png)

![image](https://user-images.githubusercontent.com/40323661/157713640-54ca854b-606f-4cfd-a03b-d3bdaac885d2.png)

![image](https://user-images.githubusercontent.com/40323661/157713690-09bccd67-d295-4151-bbb6-51877bc2b1e4.png)

#### How to use usestate & useEffect in react js

* **React Hooks**  : Hooks were added to React in version 16.8.
* Hooks allow function components to have access to state and other React features.
* The React **useState** Hook allows us to track state in a function component.
* State generally refers to data or properites that need to be tracking in an application.

![image](https://user-images.githubusercontent.com/40323661/158053942-3d6dbdd3-3a28-48f5-8fb9-d4f13d2c0bfc.png)

* Now we are seeing small project with usestate  then we will use useEffect 
* useEffect will execute after return statement execution

![image](https://user-images.githubusercontent.com/40323661/158054357-d695d870-a50d-4137-84b9-c9f0cb7a554c.png)

* Now I added useEffect hook
![image](https://user-images.githubusercontent.com/40323661/158054592-efbbfc8b-19bc-444d-8c75-05b6807e9da0.png)

*  So useEffect execute **only one time** if you not added any dependency,  let me add dependency
![image](https://user-images.githubusercontent.com/40323661/158054689-9ed11078-8582-4c3d-8be3-e91043182c20.png)

![image](https://user-images.githubusercontent.com/40323661/158054701-2d7b549f-d41e-4686-aff6-0d6b1ca9d559.png)

![image](https://user-images.githubusercontent.com/40323661/158054792-73119ac8-f6bf-492d-ad1c-5b844e4944f7.png)

#### onChange event in React

* Whenver we used onChange event with the help of useState we can get that value into variable during changing/entering the value

![image](https://user-images.githubusercontent.com/40323661/158055497-ccba244d-bb64-49a3-8b42-24c475a3d705.png)

![image](https://user-images.githubusercontent.com/40323661/158055502-3b6f1008-942c-43d8-b481-bc7db3fa234a.png)

#### How to use Map function in ReactJs 

![image](https://user-images.githubusercontent.com/40323661/158055905-6ea84b6d-e0ae-43ef-b369-d18754726372.png)

![image](https://user-images.githubusercontent.com/40323661/158056206-d94fbecc-f712-4cce-b5e1-5c87e82a3f61.png)

![image](https://user-images.githubusercontent.com/40323661/158056217-eb42b36e-4d1d-4841-87f6-7487d2b320b1.png)

![image](https://user-images.githubusercontent.com/40323661/158056258-908a9e59-38a8-448a-bd6c-cba80652d917.png)

![image](https://user-images.githubusercontent.com/40323661/158056265-6ebb33ea-c80d-4c0f-88d9-910d42c962f0.png)

* Now Array of Objects with Map
![image](https://user-images.githubusercontent.com/40323661/158056532-9c24dd84-3433-45bf-b6c1-27ad96e390bf.png)

![image](https://user-images.githubusercontent.com/40323661/158056542-8b36860c-e313-4725-976c-6e36381954a5.png)

#### How to use Filter function in ReactJs

![image](https://user-images.githubusercontent.com/40323661/158056563-0e7dc008-55bd-4267-bba6-916637f661e3.png)

![image](https://user-images.githubusercontent.com/40323661/158056790-780efe73-b9d5-4176-aac2-e41c0a5c819d.png)

![image](https://user-images.githubusercontent.com/40323661/158056806-6eabdf5a-2d64-4668-a7a4-d20d168add8a.png)

![image](https://user-images.githubusercontent.com/40323661/158056845-2de9b288-a49a-4e0a-b1dc-474f2ce6b34c.png)

![image](https://user-images.githubusercontent.com/40323661/158056854-37ef78de-62d3-4951-a21c-9c6b61091449.png)

#### How To Create Login Form With React 

* Here We are creating form and submitting using onchange and onsubmit 

```JavaScript
import React, {useState} from 'react'
import  './App.css'

const App = () => {

  const [data, setData] = useState({
     username:'',
     password:''

  })
   const {username, password}=data;
   
   const changeHandler = e=>{
     setData({...data, [e.target.name] :[e.target.value]})
   }

   const submitHandler = e=>{
     e.preventDefault();
     console.log(data);

   } 
  return (
   
    <div >
      <center >
        <form onSubmit={submitHandler}>
            <input type="text" name="username" value={username} onChange= {changeHandler}/><br/>
            <input type="password" name="password" value={password} onChange= {changeHandler}/><br/>
            <input type = "submit" name = "submit" />
        </form>
      </center>
    </div>

  );
      }
export default App
```
![image](https://user-images.githubusercontent.com/40323661/158058503-93257d6c-949b-4ae0-a4cf-75107fc8e78f.png)


```JavaScript
import React, {useState} from 'react'
import  './App.css'

const App = () => {

  const [data, setData] = useState({
     username:'',
     email:'',
     password:'',
     confirmPassword:''

  })
   const {username, email,password, confirmPassword}=data;
   
   const changeHandler = e=>{
     setData({...data, [e.target.name] :[e.target.value]})
   }

   const submitHandler = e=>{
     e.preventDefault();
      console.log(data);
   } 
  return (
   
    <div >
      <center >
        <form onSubmit={submitHandler}>
            <input type="text" name="username" value={username} onChange= {changeHandler}/><br/>
            <input type="email" name="email" value={email} onChange= {changeHandler}/><br/>
            <input type="password" name="password" value={password} onChange= {changeHandler}/><br/>
            <input type="password" name="confirmPassword" value={confirmPassword} onChange= {changeHandler}/><br/>
            <input type = "submit" name = "submit" />
        </form>
      </center>
    </div>

  );
      }
export default App

```
![image](https://user-images.githubusercontent.com/40323661/158059245-a350773f-f218-46a9-8bee-12e31078b424.png)


