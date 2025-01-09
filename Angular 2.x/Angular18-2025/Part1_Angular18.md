# Angular 2.x Application

#### Steps
* Create Folder called Angular18
* Reference to create Angular Peoject:
* https://angular.io/cli
```text
if you want to install specific version of angular 
  npm install -g @angular/cli@18
  > npm install @angular/cli@18
  > ng new ems-web-ui
 for running app
 > ng serve
```
![image](https://github.com/user-attachments/assets/b536f318-29b7-4563-b0c0-8403b45c87c4)

* Now you can add angular material
```text
ng add @angular/material
```
* To comunicate web-ui application to backend application need to create one proxy where we can define the backend urls
  
* Now create employee module
  
-------------------------------------------------------------------

#### Create proxy.config.json for defining taget URL

```text
{
    "/api":{
        "target":"http://localhost:8084",
        "secure": false
    }
}
```
* And above file put in angular.json flie under serve, after builder
 ```text
 "options": {
            "proxyConfig": "src/proxy.config.json"
          },
``` 
--------------------------------------------------------------------
#### Creating employee module and components

```text
  to create empolee module
  ng g module emploee
  
```



