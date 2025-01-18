# Angular 19 part-3 Data Binding

```text
 * How to declare a variable / state in component ?
 * What is Data Binding ?
 * What is one way Data Binding ?
      interpolation
      propertyBinding
      event binding
 * What is two way data binding ?
     using ngModel directive
 * For Desgning UI bootstrap 
```

* Just we are creating dataBinding compenent and rendering from app component
* Right now we are not creating or adding router

![image](https://github.com/user-attachments/assets/a48900b2-7c9d-4684-9a63-8a9e690ca7c9)

* This is from app component ts file
![image](https://github.com/user-attachments/assets/10f6d41b-ccbc-4b89-9920-8f6c2ec30c51)

* this is from app component .hmpl ts file

![image](https://github.com/user-attachments/assets/69ce3ac5-bf09-468e-8e81-fa9106771880)

![image](https://github.com/user-attachments/assets/6c03b65b-021c-4db7-9041-3a9cc96e7377)

* This is from data binding html component

![image](https://github.com/user-attachments/assets/cdf4dbb1-2762-4ef7-a51e-d5f590ce143d)


#### For Desgning UI bootstrap

```text
https://www.npmjs.com/package/bootstrap
cmd: npm i bootstrap
go to parent/root folder
run above comd
copy from node modules and add angular.json file under style
"./node_modules/bootstrap/dist/css/bootstrap-grid.min.css",

like below

 "styles": [
              "@angular/material/prebuilt-themes/azure-blue.css",
              "./node_modules/bootstrap/dist/css/bootstrap-grid.min.css",
              "src/styles.css"
            ],

```
#### How to declare a variable / state in component 


