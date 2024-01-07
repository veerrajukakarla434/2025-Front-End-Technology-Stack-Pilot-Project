# ems-ui project

* Added front end working classes all

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/4cde5bd6-ee87-40ba-81f3-2c34dae26096)

* **App.jsx**

```javascript
import "./App.css";
import "bootstrap/dist/css/bootstrap.min.css";
import ListEmployeeComponent from "./components/ListEmployeeComponent";
import HeaderComponent from "./components/HeaderComponent";
import FooterComponent from "./components/FooterComponent";
import { BrowserRouter, Routes, Route } from "react-router-dom";
import EmployeeComponent from "./components/EmployeeComponent";

function App() {
  return (
    <>
      <BrowserRouter>
        <HeaderComponent />
        <Routes>
          <Route path="/" element={<ListEmployeeComponent />}></Route>
          <Route path="/employees" element={<ListEmployeeComponent />}></Route>
          <Route path="/add-employee" element={<EmployeeComponent />}></Route>
          <Route path="/edit-employee/:id" element={<EmployeeComponent />} ></Route>
          <Route path="/delete-employee/:id" element={<EmployeeComponent />} ></Route>
        </Routes>
        <FooterComponent />
      </BrowserRouter>
    </>
  );
}

export default App;


```
* **HeaderComponent.jsx**

```javascript
import React from "react";

const HeaderComponent = () => {
  return (
    <div>
      <nav className="navbar navbar-dark bg-dark">
        <a className="navbar-brand" href="https://www.youtube.com/vkakarla">
          Employee Management System
        </a>
      </nav>
    </div>
  );
};

export default HeaderComponent;

```
* FooterComponent.jsx

```javascript
import React from "react";

const FooterComponent = () => {
  return (
    <div>
      <footer className="footer">
        <span>All rights are reserved for Vkakarla</span>
      </footer>
    </div>
  );
};

export default FooterComponent;

```

*** App.css**

```javascript
 .footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 50px;
  background-color: black;
  text-align: center;
  color: white;
}


```
* ListEmployeeComponent.jsx

```javascript
import { useEffect, useState } from "react";
import React from "react";
import { deleteEmployee, listEmployees } from "../services/EmployeeService";
import { useNavigate } from "react-router-dom";

const ListEmployeeComponent = () => {
  const [empployees, setEmployees] = useState([]);
  const navigator = useNavigate();
  useEffect(() => {
    getAllEmployees();
  }, []);

   function getAllEmployees(){
    listEmployees()
    .then((response) => {
      setEmployees(response.data);
    })
    .catch((error) => {
      console.error(error);
    });
  }

  function addNewEmployee() {
    navigator("/add-employee");
  }

  function updateEmployee(id) {
    navigator(`/edit-employee/${id}`);
  }

  function removeEmployee(id) {
   deleteEmployee(id).then((response)=>{
    getAllEmployees();
   }).catch(error=>{
    console.error(error);
   })
  }

  return (
    <div className="container">
      <h2 className="text-center">List Of Employees</h2>
      <button className="btn btn-primary mb-2" onClick={addNewEmployee}>
        Add Employee
      </button>
      <table className="table table-striped table-bordered">
        <thead>
          <tr>
            <th>Employee Id</th>
            <th>Employee first Name</th>
            <th>Employee Last Name</th>
            <th>Employee Department</th>
            <th>Employee Email Id</th>
            <th>Employee Adress</th>
            <th>Actions</th>
          </tr>
        </thead>

        <tbody>
          {empployees.map((employee) => (
            <tr key={employee.id}>
              <td>{employee.id}</td>
              <td>{employee.firstName}</td>
              <td>{employee.lastName}</td>
              <td>{employee.department}</td>
              <td>{employee.email}</td>
              <td>{employee.address}</td>
              <td>
                <button className="btn btn-info mb-2" onClick={() => updateEmployee(employee.id)}>Update</button> 
                <button className="btn btn-danger mb-2" onClick={() => removeEmployee(employee.id)} 
                style={{marginLeft:'10px'} }>Delete</button>
              </td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
};

export default ListEmployeeComponent;

```
* EmployeeComponent.jsx

```javascript
import React, { useEffect } from "react";
import { useState } from "react";
import {
  createEmployee,
  deleteEmployee,
  getEmployee,
  updateEmployee,
} from "../services/EmployeeService";
import { useNavigate, useParams } from "react-router-dom";

const EmployeeComponent = () => {
  const [firstName, setFirstName] = useState("");
  const [lastName, setLastName] = useState("");
  const [department, setDepartment] = useState("");
  const [email, setEmail] = useState("");
  const [address, setAddress] = useState("");

  const { id } = useParams();

  const [errors, setErrors] = useState({
    firstName: "",
    lastName: "",
    department: "",
    email: "",
    address: "",
  });

  const navigator = useNavigate();

  useEffect(() => {
    if (id) {
      getEmployee(id)
        .then((response) => {
          setFirstName(response.data.firstName);
          setLastName(response.data.lastName);
          setDepartment(response.data.department);
          setEmail(response.data.email);
          setAddress(response.data.address);
        })
        .catch((error) => {
          console.log(error);
        });
    }
  }, [id]);


  function saveOrUpdateEmployee(e) {
    e.preventDefault();

    if (validateForm()) {
      const employee = { firstName, lastName, department, email, address };
      console.log(employee);
      if (id) {
        updateEmployee(id, employee)
          .then((response) => {
            console.log(response.data);
            navigator("/employees");
          })
          .catch((error) => {
            console.error(error);
          });
      } else {
        createEmployee(employee)
          .then((response) => {
            navigator("/employees");
          })
          .catch((error) => {
            console.error(error);
          });
      }
    }
  }

  function validateForm() {
    let valid = true;
    const errorCopy = { ...errors };

    if (firstName.trim()) {
      errorCopy.firstName = "";
    } else {
      errorCopy.firstName = "First name is required";
      valid = false;
    }

    if (lastName.trim()) {
      errorCopy.lastName = "";
    } else {
      errorCopy.lastName = "Last name is required";
      valid = false;
    }

    if (department.trim()) {
      errorCopy.department = "";
    } else {
      errorCopy.department = "Department is required";
      valid = false;
    }

    if (email.trim()) {
      errorCopy.email = "";
    } else {
      errorCopy.email = "Email is required";
      valid = false;
    }

    if (address.trim()) {
      errorCopy.address = "";
    } else {
      errorCopy.address = "Address is required";
      valid = false;
    }

    setErrors(errorCopy);
    return valid;
  }

  function pageTitle() {
    if (id) {
      return <h2 className="text-center">Update Employee</h2>;
    } else {
      return <h2 className="text-center">Add Employee</h2>;
    }
  }

  return (
    <div className="container">
      <br />
      <br />
      <div className="row">
        <div className="card col-md-6 offset-md-3 offset-md-3">
          {pageTitle()}
          <div className="card-body">
            <form>
              <div className="form-group mb-2">
                <label className="form-lable">First Name:</label>
                <input
                  type="text"
                  placeholder="Enter Employee First Name"
                  value={firstName}
                  className={`form-control ${
                    errors.firstName ? "is-invalid" : ""
                  }`}
                  onChange={(e) => setFirstName(e.target.value)}
                ></input>
                {errors.firstName && (
                  <div className="invalid-feedback"> {errors.firstName}</div>
                )}
              </div>
              <div className="form-group mb-2">
                <label className="form-lable">Last Name:</label>
                <input
                  type="text"
                  placeholder="Enter Employee Last Name"
                  value={lastName}
                  className={`form-control ${
                    errors.lastName ? "is-invalid" : ""
                  }`}
                  onChange={(e) => setLastName(e.target.value)}
                ></input>
                {errors.lastName && (
                  <div className="invalid-feedback"> {errors.lastName}</div>
                )}
              </div>
              <div className="form-group mb-2">
                <label className="form-lable">DepartMent:</label>
                <input
                  type="text"
                  placeholder="Enter Employee Department"
                  value={department}
                  className={`form-control ${
                    errors.department ? "is-invalid" : ""
                  }`}
                  onChange={(e) => setDepartment(e.target.value)}
                ></input>
                {errors.department && (
                  <div className="invalid-feedback"> {errors.department}</div>
                )}
              </div>
              <div className="form-group mb-2">
                <label className="form-lable">Email:</label>
                <input
                  type="text"
                  placeholder="Enter Employee Email"
                  value={email}
                  className={`form-control ${errors.email ? "is-invalid" : ""}`}
                  onChange={(e) => setEmail(e.target.value)}
                ></input>
                {errors.email && (
                  <div className="invalid-feedback"> {errors.email}</div>
                )}
              </div>

              <div className="form-group mb-2">
                <label className="form-lable">Address:</label>
                <input
                  type="text"
                  placeholder="Enter Employee Address"
                  value={address}
                  className={`form-control ${
                    errors.address ? "is-invalid" : ""
                  }`}
                  onChange={(e) => setAddress(e.target.value)}
                ></input>
                {errors.address && (
                  <div className="invalid-feedback"> {errors.address}</div>
                )}
              </div>

              <button
                className="btn btn-success"
                onClick={saveOrUpdateEmployee}
              >
                Submit
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  );
};

export default EmployeeComponent;

```
* **EmployeeService.js**
```javascript
import axios from "axios";

const REST_API_BASE_URL = "http://localhost:2024/api/employees";

export const listEmployees = () => axios.get(REST_API_BASE_URL);

export const createEmployee = (employee) => axios.post(REST_API_BASE_URL, employee);

export const getEmployee = (employeeId) => axios.get(REST_API_BASE_URL + "/" + employeeId);

export const updateEmployee = (employeeId, employee) => axios.put(REST_API_BASE_URL + "/" + employeeId, employee);

export const deleteEmployee = (employeeId) => axios.delete(REST_API_BASE_URL + '/'+employeeId);
```
