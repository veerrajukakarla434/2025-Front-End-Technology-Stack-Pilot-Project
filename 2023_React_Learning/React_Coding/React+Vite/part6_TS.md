# Conditionally Rendering JSX & Components

* App.tsx

```javascript
import ConditionalComponent from "./components/ConditionalComponent";
import Fruits from "./components/Fruits";

function App() {
  return (
    <div className="App">
      <ConditionalComponent />
    </div>
  );
}

export default App;
```

* ConditionalComponent.tsx

```javascript
export default function ConditionalComponent() {
  const diaplay = true;
  if (diaplay) {
    return (
      <div>
        <h1>This is ConditionalComponent</h1>
      </div>
    );
  } else {
    return (
      <div>
        <h1>Code is EveryDay!</h1>
      </div>
    );
  }
}

```
  
* Output:

  ![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/90d36599-bd78-4fb0-bcd1-28f4cf8fdf06)

* If We add as components instead of statements
* App.tsx
  
```javascripts
import ConditionalComponent from "./components/ConditionalComponent";

function App() {
  return (
    <div className="App">
      <ConditionalComponent />
    </div>
  );
}

export default App;
```

* ConditionalComponent.tsx
  
```javascripts
import Code from "./Code";
import Welcome from "./Welcome";

export default function ConditionalComponent() {
  const diaplay = false;
  if (diaplay) {
    return <Welcome />;
  } else {
    return <Code />;
  }
}
```
* Welcome.tsx
  
```javascript
export default function Welcome() {
  return (
    <div>
      <h1>You Are Welcome</h1>
    </div>
  );
}

```
* Code.tsx
  
```javascript
  export default function Code() {
  return (
    <div>
      <h1>Code EveryDay!!</h1>
    </div>
  );
}

```
 
* Output:

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/4207a1ae-9707-4bc7-839b-7684c7ea6504)

* Here the problem is should return more than one from a function as components.
* So Elements will come in to this picture
* You can use single return statement in component or adding elements
* ConditionalComponent.tsx  
```javascript
import Code from "./Code";
import Welcome from "./Welcome";

export default function ConditionalComponent() {
  let message;
  const diaplay = true;
  if (diaplay) {
    message = <Welcome />; //  <h1>You Are Welcome</h1>
  } else {
    message = <Code />; //<h1>Code EveryDay!!</h1>
  }

  return message;
}
```
