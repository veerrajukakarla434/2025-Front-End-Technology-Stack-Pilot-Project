## Creating React Application 

* Step1 to create ReactJs with Vite run below command
    * npm create vite@4.1.0  or npm create vite@latest
* Give the project name then select Rect then select TypeScript

 ![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/8783320e-2c4f-42fc-b05b-c3cd9eca027a)

* Run the below commands

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/345aeb81-f161-4cbd-9c82-52cd821805b5)

* Run npm run dev  command
  
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/c2d769a4-56ca-4066-a484-e6a170f42fd7)

 * Open ths url to see the project http://127.0.0.1:5173/

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/c0bb08a6-776f-4c34-9371-9ee8c927324b)

* if you want to exit or stop the application  press Ctrl+C application will stop
 
#### Project Structure 

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/cba679ac-2f40-411a-a6ec-50e2a3783e27)

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/9fe6e419-2b3d-4170-9219-568059be4f79)

* After deleting unwanted file to understand in simple way

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/1f945d09-19b6-476e-b17c-bb9fa5796892)

* index.html
```java
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite + React + TS</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
  </body>
</html>

```
* App.tsx
```java
function App() {
  return (
    <div className="App">Hello World : Welcome To ReactJS Application</div>
  );
}

export default App;
```
* main.tsx
```java
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

ReactDOM.createRoot(document.getElementById("root") as HTMLElement).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```
* Now the Output

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/ec335f7d-6600-4591-a8de-19744d89b546)
