# 2022-Front-End-Training
#### Tech Stack

* **Note** : Follow above folders and documents based on below sequence 
 
 * HTML With CSS
 * Java Script & Type Script
 * React JS (Node Js & Express JS)
 * Angular 2.x
 * Full Stack Application Srping Boot + MongoDB + ReactJs
 * Full Stack Application Spring Boot + MongoDB + Angular 7/8

   ```javaScript
    import { useState } from "react";


export const MultipleInputValues = () => {
    const [formData, setFormData] = useState(
        {
            firstName: "",
            lastName: "",
            email: ""
        });
    
        const handleChange = (event: any) => {
            const {name, value } = event.target;
            setFormData((prevFormData) => ({ ...prevFormData, [name]: value }));
          };
        
          const handleSubmit = (event: any) => {
            event.preventDefault();
             console.log(formData.firstName,  formData.lastName,  formData.email)
           
        };   
   
  return (
    <>
    <form onSubmit={handleSubmit}>
       <label htmlFor="name">First Name:</label>
       <input type="text" id="firstName" name="firstName" value={formData.firstName} onChange={handleChange}/> <br/>
      
      <label htmlFor="message">Last Name:</label>
      <input type="text" id="lastName" name="lastName" value={formData.lastName} onChange={handleChange}/><br/>
      
      <label htmlFor="email">Email:</label>
      <input type="email" id="email" name="email" value={formData.email} onChange={handleChange}/><br/>

      <button type="submit" color="blue">Submit</button>
     </form>
       
    </>
  )
}

   ```


* Form Validations:

```javascript
import { useState } from 'react'

export const MultipleInputValuesWithValidations = () => {
     const [firstName, setFirstName]= useState('')
     const [lastName, setLastName]= useState('')
     const [email, setEmail]= useState('')

        const [errors, setErrors]=useState({
            firstName:"",
            lastName:"",
            email:""
           })

          const handleSubmit = (event: any) => {
            event.preventDefault();
            valiDateForm();
        };   

     function valiDateForm(){
        const employee ={firstName,lastName,email};
        console.log(employee);

        let valid = true;
        const errorsCopy = {...errors};
        
        if(firstName.trim()){
            errorsCopy.firstName="";
           }else{
            errorsCopy.firstName="FirstName is required";
            valid=false;
           }

           if(lastName.trim()){
            errorsCopy.lastName="";
           }else{
            errorsCopy.lastName="LastName is required";
            valid=false;
           }
  
           if(email.trim()){
            errorsCopy.email="";
           }else{
            errorsCopy.email="Email is required";
            valid=false;
           }

           setErrors(errorsCopy);
           return valid;
     }


   
  return (
    <>
    <form onSubmit={handleSubmit}>
       <label htmlFor="name">First Name:</label>
       <input 
       type="text" 
       name="firstName" 
       value={firstName} 
       className={`form-control ${errors.firstName ? 'is-invalid' : ""}`}
       onChange={(e)=> setFirstName(e.target.value)}/><br/>
       {errors.firstName && (<div className="invalid-feedback">{errors.firstName}</div> )}

       <label htmlFor="name">Last Name:</label>
       <input 
       type="text" 
       name="lastName" 
       value={lastName} 
       className={`form-control ${errors.lastName ? 'is-invalid' : ""}`}
       onChange={(e)=> setLastName(e.target.value)}/><br/>
       {errors.lastName && (<div className="invalid-feedback">{errors.lastName}</div> )}


       <label htmlFor="name">Email:</label>
       <input 
       type="text" 
       name="email" 
       value={email} 
       className={`form-control ${errors.email ? 'is-invalid' : ""}`}
       onChange={(e)=> setEmail(e.target.value)}/><br/>
       {errors.email && (<div className="invalid-feedback">{errors.email}</div> )}
     
      <button type="submit" color="blue">Submit</button>
     </form>
       
    </>
  )
}

```



 
