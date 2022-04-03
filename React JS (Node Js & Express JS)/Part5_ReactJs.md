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


