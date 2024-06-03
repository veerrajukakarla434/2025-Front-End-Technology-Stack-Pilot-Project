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
 
