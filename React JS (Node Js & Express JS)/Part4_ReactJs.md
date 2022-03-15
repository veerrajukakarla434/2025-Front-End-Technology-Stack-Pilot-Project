## React Advanced 

* #### How To Create Calculator React App

```JavaScript
import React, {useState} from 'react'
import  './App.css'

const App = () => {

  const [input, setInput] = useState("");
  const [result, setResult] = useState(0);
  const handler = e =>{
    setInput(e.target.value);
  }
  return (
   
    <div >
     <center>
        <input type="text"  value={input} name="input" onChange={handler}/>
        <br/>
        <button onClick={()=> setResult(eval(input))}>Result</button>
      <h4>Result is : {result}</h4>

      <button onClick={() => setInput(input+'1')}>1</button>
        <button onClick={() => setInput(input+'2')}>2</button>
        <button onClick={() => setInput(input+'3')}>3</button>
        <button onClick={() => setInput(input+'4')}>4</button>
        <button onClick={() => setInput(input+'5')}>5</button><br />
        
        <button onClick={() => setInput(input+'6')}>6</button>
        <button onClick={() => setInput(input+'7')}>7</button>
        <button onClick={() => setInput(input+'8')}>8</button>
        <button onClick={() => setInput(input+'9')}>9</button>
        <button onClick={() => setInput(input+'0')}>0</button><br />

        <button onClick={() => setInput(input+'+')}>+</button>
        <button onClick={() => setInput(input+'-')}>-</button>
        <button onClick={() => setInput(input+'*')}>*</button>
        <button onClick={() => setInput(input+'/')}>/</button>
        <button onClick={() => {setInput('');setResult(0)}}>clr</button><br /> 
     

     </center>
    </div>

  );
      }
export default App


```
![image](https://user-images.githubusercontent.com/40323661/158420502-1840dc30-5fb2-475f-8b55-1061f4c25160.png)

#### React Router

* Routing is a process in which a user is directed to different pages based on their action or request. 
* ReactJS Router is mainly used for developing Single Page Web Applications. 
* React Router is used to define multiple routes in the application. When a user types a specific URL into the browser, and if this URL path matches any 'route' inside the router file, the user will be redirected to that particular route.

![image](https://user-images.githubusercontent.com/40323661/158422358-4fe7157a-9575-4eae-836b-cc60b76bb3d5.png)

![image](https://user-images.githubusercontent.com/40323661/158422507-8a30efe5-00b0-47c3-9459-9b6f44234963.png)



