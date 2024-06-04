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

* React hook with form values

```javascript

  import { useForm } from "react-hook-form"
import {DevTool} from "@hookform/devtools"

export const ReactHookForm123 = () => {

    type FormValues = {
        firstName: string;
        lastName: string;
        email: string;
    }

    const form = useForm<FormValues>();
    const { register , control, handleSubmit } = form
   

    const onSubmit = (data: FormValues)=> {
        console.log('Form Submited', data);
    };

    return (
        <div>
            <form onSubmit={handleSubmit(onSubmit)}>
              
                <label htmlFor="firstNamen">First Name:</label>
                <input type="text"  id="firstName"  {...register("firstName")}/> <br/>
                
                <label htmlFor="lastName">Last Name:</label>
                <input type="text"  id="lastName"  {...register("lastName")}/> <br/>
                
                <label htmlFor="email">Email:</label>
                <input type="text"  id="email"  {...register("email")}/> <br/>

                <button>Submit</button>
            </form>
            <DevTool control={control} />
        </div>
    )
}

```

* With Validations:

```javascript

import { useForm } from "react-hook-form"
import {DevTool} from "@hookform/devtools"

export const ReactHookForm123WithValidations = () => {

    type FormValues = {
        firstName: string;
        lastName: string;
        email: string;
    }

    const form = useForm<FormValues>();
    const { register , control, handleSubmit , formState} = form
    const {errors} = formState;
   
    const onSubmit = (data: FormValues)=> {
        console.log('Form Submited', data);
    };





    return (
        <div>
            <form onSubmit={handleSubmit(onSubmit)} noValidate>
              
                <label htmlFor="firstNamen">First Name:</label>
                <input 
                type="text"  
                id="firstName"  
                {...register("firstName", {
                    required:{
                        value: true,
                        message:'firstName is required'}
                    })}/> <br/>
                 <p>{errors.firstName?.message}</p>

                <label htmlFor="lastName">Last Name:</label>
                <input type="text"  
                id="lastName"  
                {...register("lastName", {
                    required:{
                        value: true,
                        message:'lastName is required'}

                    })}/> <br/>
                <p>{errors.lastName?.message}</p>

                <label htmlFor="email">Email:</label>
                <input type="text"  
                id="email"  
                {...register("email", {
                    pattern:{
                        value: /^[^\s@]+@[^\s@]+\.[^\s@]+$/,
                        message:'Invalid Email Formate'
                    }

                    })}/> <br/>
                 <p>{errors.email?.message}</p>

                <button>Submit</button>
            </form>
            <DevTool control={control} />
        </div>
    )
}
```
 
