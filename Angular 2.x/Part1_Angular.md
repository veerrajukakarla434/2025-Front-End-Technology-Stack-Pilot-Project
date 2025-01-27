## Angular 2.x  (Initial learning) 

* Reference to create Angular Peoject:
  * https://angular.io/cli

    
```javascript
 Alt + Shift + F  for code formate
  for latest version npm install -g @angular/cli
  if you want to install specific version of angular
  npm install -g @angular/cli@16.2.1
  > npm install @angular/cli@16
  > ng new ems-frontend


  ng new ems-ui
  npm install
  npm install bootstrap jquery
  ng add @angular/material

```



    ```javascript
     ng g c components/header
     ng g c components/home
     ng g c components/post-employee
     ng g c components/get-allemployees
     ng g c components/update-employee
     ng g c components/delete-employee
     ng g s service/employee
    ```
* Now configure the bootstrap
  
```text
  Bootstrap steps:
1. npm install bootstrap jQuery
2. In angular.json file
   In styles array: 
        "src/styles.css",
        "node_modules/bootstrap/dist/css/bootstrap.min.css"
   In scripts array:
        "node_modules/jquery/dist/jquery.min.js",
        "node_modules/bootstrap/dist/js/bootstrap.min.js"

Material UI steps:
1. ng add @angular/material
2. Choose theme and we are good to go
```    

* Add routing to the header and home components in app-routing-module.ts

  ![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/e3cb1abe-1bf5-479b-a2a9-15ac688c7402)

* Now app.module.ts will be updated like this

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/cfd2a909-885c-4b31-8556-5a307b76f51e)

* Now home page looks like this

  ![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/8b0e0558-a9fd-41fd-9417-acb303aba969)


![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/f2fc8fd4-1f6a-4e61-9eea-aadc1756d832)


![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/87d1af7f-093d-42df-9954-978b2a1112cd)


![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/b0f3c503-9d4b-4220-b892-42e6977d164b)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/f631c973-1a87-42d9-b2fa-c8ed01c71d9c)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/ce8fc29c-6d77-49c7-a5fb-3da2a5653716)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/b2604163-704f-423f-98bf-3048d2becc26)


