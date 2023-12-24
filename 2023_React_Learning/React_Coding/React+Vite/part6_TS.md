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
