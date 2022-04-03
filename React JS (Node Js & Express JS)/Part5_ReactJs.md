## CRUD Example Using Axios

* We have APP.js below after simplefied 
 ![image](https://user-images.githubusercontent.com/40323661/161406204-fdea1a11-4427-4b76-9b6d-6a54916d8f6a.png)
 
 * Out Put will be 

![image](https://user-images.githubusercontent.com/40323661/161406242-49f40a32-fef6-4b70-bd60-38494813998d.png)

#### React Bootstrap

* Now we can add  **React Bootstrap** for style designing 

* Single-page applications gaining popularity over the last few years, so many front-end frameworks have introduced such as Angular, React, Vue.js, Ember, etc. As a result, jQuery is not a necessary requirement for building web apps. Today, React has the most used JavaScript framework for building web applications, and Bootstrap become the most popular CSS framework. So, it is necessary to learn various ways in which Bootstrap can be used in React apps, which is the main aim of this section.

![image](https://user-images.githubusercontent.com/40323661/161406338-170049c8-5012-4ebb-86f9-de3edf2c890d.png)

![image](https://user-images.githubusercontent.com/40323661/161406357-c0ba1dd8-4e7e-4344-9630-e2b9b7b653e8.png)


```javaScript
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">  
```

![image](https://user-images.githubusercontent.com/40323661/161406486-3af0eeeb-f677-436a-9a68-ba462808960d.png)


![image](https://user-images.githubusercontent.com/40323661/161406572-c720adb6-739f-483b-a14d-2ae74ce8e3a5.png)

* Create ListEmployeeComponent.jsx and add below code

```JavaScript
import React, { Component } from 'react'

export default class ListEmployeeComponent extends Component {
   
    constructor(props){
        super(props)

        this.state = {
             employee:[]
        }
    }


  render() {
    return (
      <div>
             <h2 className='text-center'>Employee List</h2>
             <div className='row'>
                <table className='table table-striped table-boarded'>  
                  <thead>
                    <tr>
                       <th>Employee First Name</th>
                       <th>Employee Last Name</th>
                       <th>Employee Email ID</th>
                       <th>Employee Department</th>
                       <th>Employee Address</th>
                       <th>Actions</th>
                    </tr>  
                  </thead>
                  <tbody>
                    {
                        this.state.employee.map(
                            employee =>
                            <tr key={employee.id}>
                               <td>{employee.firstName}</td>
                               <td>{employee.lastName}</td>
                               <td>{employee.email}</td>
                               <td>{employee.department}</td>
                               <td>{employee.address}</td>
                            </tr>
                        )
                    }

                  </tbody>

                </table>
             </div>
      </div>
    )
  }
}
```

![image](https://user-images.githubusercontent.com/40323661/161407881-662da696-8088-4ab7-8ba2-3c2d6ddc030f.png)


![image](https://user-images.githubusercontent.com/40323661/161407878-2ce46736-9ea8-44b3-bb39-9adc853904c6.png)

* To call/load dynamic list to our application we need to install react external call libraries called **Axios**
* instalation command is npm install axios --save

![image](https://user-images.githubusercontent.com/40323661/161409179-fd2f5a8a-5a1b-47e7-938f-b76877e908ce.png)

![image](https://user-images.githubusercontent.com/40323661/161409192-d7bc4b1b-3572-4cf5-b761-9e9b78e3ef8f.png)

![image](https://user-images.githubusercontent.com/40323661/161409174-33197a9e-42bb-47c9-8d04-8f3e9d53b1bd.png)

* Added Header and footer cpmonents along with service component

```JavaScript

import React from 'react';


class FooterComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {};
    }

    render() {
        return (
            <div>
                <footer >
                <nav className="navbar navbar-expand-md navbar-dark bg-dark">
                      <span className='text-muted'> All Rights Resverved 2022 @Vkakarla</span>
                </nav>
                </footer>
            </div>
        );
    }
}


export default FooterComponent;

=====================================================================
import React from 'react';


class HeaderComponent extends React.Component {
    constructor(props) {
        super(props);
        this.state = {};
    }

    render() {
        return (
            <div>
                <header>
                    <nav className="navbar navbar-expand-md navbar-dark bg-dark">
                     <div> <a href='https://www.youtube.com/c/vkakarla' className='navbar-brand'> Employee Management Application</a></div>
                    </nav>
                </header>  
            </div>
        );
    }
}



export default HeaderComponent;
====================================================================
import React, { Component } from 'react'
import EmployeeService from '../services/EmployeeService'

export default class ListEmployeeComponent extends Component {
   
    constructor(props){
        super(props)

        this.state = {
             employee:[]
        }
    }

   componentDidMount(){
       EmployeeService.getEmployees().then((res) =>{
          this.setState({employee: res.data});
       });
   }
  render() {
    return (
      <div className='container'>
             <h2 className='text-center'>Employee List</h2>
             <div className='row'>
                <table className='table table-striped table-boarded'>  
                  <thead>
                    <tr>
                       <th>Employee First Name</th>
                       <th>Employee Last Name</th>
                       <th>Employee Email ID</th>
                       <th>Employee Department</th>
                       <th>Employee Address</th>
                       <th>Actions</th>
                    </tr>  
                  </thead>
                  <tbody>
                    {
                        this.state.employee.map(
                            employee =>
                            <tr key={employee.id}>
                               <td>{employee.firstName}</td>
                               <td>{employee.lastName}</td>
                               <td>{employee.email}</td>
                               <td>{employee.department}</td>
                               <td>{employee.address}</td>
                            </tr>
                        )
                    }

                  </tbody>

                </table>
             </div>
      </div>
    )
  }
}

===================================================
App.css

.App {
  text-align: center;
}

.App-logo {
  height: 40vmin;
  pointer-events: none;
}

@media (prefers-reduced-motion: no-preference) {
  .App-logo {
    animation: App-logo-spin infinite 20s linear;
  }
}

.App-header {
  background-color: #282c34;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: calc(10px + 2vmin);
  color: white;
}

.App-link {
  color: #61dafb;
}

@keyframes App-logo-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.footer{
   position: absolute;
   bottom: 0;
   width: 100%;
   height: 50px;
   background-color: black;
   text-align: center;
   color: white;
}
==============================================

App.js


import './App.css';
import ListEmployeeComponent from './components/ListEmployeeComponent';
import HeaderComponent from './components/HeaderComponent';
import FooterComponent from './components/FooterComponent';

function App() {
  return (

    <div>
       <HeaderComponent />
       <div className="contrainer">
          <ListEmployeeComponent />
       </div>
       <FooterComponent />
    </div>

    
  );
}

export default App;
=================================================
index.js

import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
import reportWebVitals from './reportWebVitals';
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle.min';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();

=============================================

import axios from 'axios';

const EMPLOYEE_API_BASE_URL ="http://localhost:2023/api/v1/employee";
class EmployeeService{

     getEmployees(){
         return axios.get(EMPLOYEE_API_BASE_URL);
     }
}

export default new EmployeeService();

```

* Ouput you can see below
![image](https://user-images.githubusercontent.com/40323661/161424849-dd531c0d-b8cd-4811-8c91-8bd40b18b309.png)




