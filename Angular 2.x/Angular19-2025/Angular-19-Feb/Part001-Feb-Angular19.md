# Angular 19

```javascript

npm install -g @angular/cli
ng new EMS-WEB-UI2
npm i bootstrap

https://www.npmjs.com/package/bootstrap
cmd: npm i bootstrap
go to parent/root folder
run above comd
copy from node modules and add angular.json file under style
"./node_modules/bootstrap/dist/css/bootstrap-grid.min.css",

like below

 "styles": [
              "@angular/material/prebuilt-themes/azure-blue.css",
              "./node_modules/bootstrap/dist/css/bootstrap.min.css",
              "src/styles.css"
            ],

```
* Current or initial routes

```javascript

import { Routes } from '@angular/router';
import { LoginComponent } from './pages/login/login.component';
import { LayoutComponent } from './pages/layout/layout.component';
import { DashboardComponent } from './pages/dashboard/dashboard.component';
import { EmployeeComponent } from './pages/employee/employee.component';

export const routes: Routes = [

    {
      path:'',
      redirectTo:'login',
      pathMatch:'full'
    },
    {
        path:'login',
        component:LoginComponent
    },
    {
        path:'',
        component:LayoutComponent,
        children:[
            {
                path:'dashboard',
                component:DashboardComponent
            },
            {
                path:'empaloyee',
                component:EmployeeComponent
            }
        ]
    },

];

  ```
