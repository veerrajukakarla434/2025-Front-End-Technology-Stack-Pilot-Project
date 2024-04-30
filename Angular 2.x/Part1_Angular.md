## Angular 2.x  (Initial learning) 

* Reference to create Angular Peoject:
  * https://angular.io/cli
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
    
```javascript

  if you want to install specific version of angular 
  npm install -g @angular/cli@16.2.1

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

    
