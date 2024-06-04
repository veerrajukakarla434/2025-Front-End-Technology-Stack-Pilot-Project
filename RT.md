```javascript


Steps to install React :
------------------------

npm create vite@latest WFT-UI

cd WFT-UI
npm install
npm run dev

https://mui.com/material-ui/getting-started/installation/

npm install @mui/material @emotion/react @emotion/styled



Controlled Components in React

Example1
----------
import {useState} from 'react';
 
export default function  ControlledComponent()  {
	const  [inputValue, setInputValue] =  useState('');

	const  handleChange = (event) => {
		setInputValue(event.target.value);
	};

return  (
<form>
	<label>Input Value:
	<input  type="text"  value={inputValue} onChange={handleChange} />
	</label>
	<p>Input Value: {inputValue}</p>
</div>
)};

--------------------------------------

OR  We can write Hancdle change function in input tag it self
------------------------------------------------------------
import { useState } from "react"

export const Home = () => {
  
    const [inputValue, setInputValue] = useState('');
        
  return (
    <div>
      <form>
        <label> Input Value:</label>
        
        <input type="text" 
        value={inputValue} 
        onChange={(event: any)=> setInputValue(event.target.value)}/>

        <p> Input Vache What you entered: {inputValue}</p>
      </form>

    </div>
  )
}
-------------------------------------------------------------

As the user types into the input field, the handleChange function updates the state variable using the "setInputValue" function. The component is then re-rendered, and the input field's value attribute is updated to reflect the new value of inputValue.

The value of the input field and the text displayed below it are always in sync, making it a controlled component.


How to handle dropdowns and checkboxes in Controlled Components
-------------------------------------------------------------


function Checkbox() {
  const [isChecked, setIsChecked] = useState(false);

  const handleChange = (event) => {
    setIsChecked(event.target.checked);
  };

  return (
    <form>
      <label htmlFor="color">
        <input type="checkbox" name="color" checked={isChecked} onChange={handleChange}/>
        Blue
      </label>

      {isChecked && <div>Blue is selected!</div>}
    </form>
  );
}

export default Checkbox;



Droup down:
----------
import { useState } from "react";

export default function Dropdown()  {
	const [selectedOption, setSelectedOption] = useState("option1");

	const  handleDropdownChange = (event) => {
		setSelectedOption(event.target.value);
	};

return  (
	<div>
		<label>
			Select an option:
				<select  value={selectedOption} onChange={handleDropdownChange}>
				<option  value="option1">Option 1</option>
				<option  value="option2">Option 2</option>
				<option  value="option3">Option 3</option>
			</select>
		</label>
		<p>Selected option: {selectedOption}</p>
	</div>
	);
}

----------------------------------------------------


Multiple input values  and its validations:




The useState hook defines a state object named formData that contains three properties: name, email, and message, each initialized to an empty string.

The handleChange function is called whenever a user types in one of the form fields. It extracts the name and value of the form field that has changed using the event.target object and then updates the formData state variable using the setFormData function.

The setFormData function uses the spread operator (...) to copy the previous formData object. Then it updates the value of the changed form field by setting its value prop with the new value.

By using an object to manage form data, we can easily keep track of the values of multiple form elements. This makes it easier to manage and manipulate the state of our form data, especially when dealing with complex forms with many form elements.


Without validations
-------------------
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
--------------------------------------------



With Validations
------------------------------------------------

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

-------------------------------------------------

react-hook-form
--------------

npm install @hookform/devtools -D


what is the form state:

every form has few moving parts while user enter the input values

current values of every field of a form
whether the filed hasbeen interacted With
whether the filed value is changed
whether is the form is invalid
whether the field contains error  ae collectively called form state







register an input or select element and apply validation rules to React Hook Form. 
Validation rules are all based on the HTML standard
and also allow for custom validation methods.


const { onChange, onBlur, name, ref } = register('firstName'); 
// include type check against field path with the name you have supplied.
        
<input 
  onChange={onChange} // assign onChange event 
  onBlur={onBlur} // assign onBlur event
  name={name} // assign name prop
  ref={ref} // assign ref prop
/>
// same as above
<input {...register('firstName')} />


import { useForm } from "react-hook-form"


export const RhF123 = () => {

  const form = useForm();
  const {register} = form;
  const {name, ref, onChange, onBlur} = register("firstName");

  return (
    <div>
     <form>
     <label htmlFor="firstNamen">First Name:</label>
      <input 
      type="text"  
      id="firstName"  
      name={name}
      ref={ref}
      onChange={onChange}
      onBlur={onBlur}/> <br/>

     </form>


    </div>
  )
}

We can directly use like below
--------------------------

import { useForm } from "react-hook-form"


export const RhF123 = () => {

  const form = useForm();
  const {register} = form;
  

  return (
    <div>
     <form>
     <label htmlFor="firstNamen">First Name:</label>
      <input 
      type="text"  
      id="firstName"  
      {...register("firstNamen")}/> <br/>

     </form>


    </div>
  )
}





Two fields

touthc : whether the interactor With
dirthy : weather the field value is changed


Now we will se the form state
-----------------------------


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
                <input type="text"  
				id="firstName" 
				na
				
				/> <br/>
                
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

--------------------------------------------------------

React Hook Forms support HTML validations rules
including

required
minLenght & MaxLenght
min & max
pattern

Lest start a basic validation rule for firstName

lest add 
noValidate attribute to the form 
this vill prevent brower validation and allow react hook to validate fom fields





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
                    required:'firstName is required'

                    })}/> <br/>
               

                <label htmlFor="lastName">Last Name:</label>
                <input type="text"  
                id="lastName"  
                {...register("lastName", {
                    required:'lastName is required'

                    })}/> <br/>
               

                <label htmlFor="email">Email:</label>
                <input type="text"  
                id="email"  
                {...register("email", {
                    required:'email is required'

                    })}/> <br/>
               

                <button>Submit</button>
            </form>
            <DevTool control={control} />
        </div>
    )
}



This is for developer exp for better understanding how the validation is happing


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
    // errors object will contains individuval feild error info/ messages
	
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
               

                <label htmlFor="lastName">Last Name:</label>
                <input type="text"  
                id="lastName"  
                {...register("lastName", {
                    required:{
                        value: true,
                        message:'lastName is required'}

                    })}/> <br/>
               

                <label htmlFor="email">Email:</label>
                <input type="text"  
                id="email"  
                {...register("email", {
                    pattern:{
                        value: /^[^\s@]+@[^\s@]+\.[^\s@]+$/,
                        message:'Invalid Email Formate'
                    }

                    })}/> <br/>
               

                <button>Submit</button>
            </form>
            <DevTool control={control} />
        </div>
    )
}

for end user exp let add error message


WIth Validations:


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
