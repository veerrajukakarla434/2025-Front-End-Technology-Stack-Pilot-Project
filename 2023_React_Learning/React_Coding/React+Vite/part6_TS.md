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
