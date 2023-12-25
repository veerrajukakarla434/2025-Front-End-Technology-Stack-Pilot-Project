# Event Handling In React

* Just like HTML DOM events, React can perform actions based on user events.
* React has the same events as HTML: click, change, mouseover etc.

* **Adding Events**
* React events are written in **camelCase syntax**:
  
```javascript
onClick instead of onclick.
```
* React event handlers are written **inside curly braces:**

```javascript
onClick={shoot}  instead of onClick="shoot()".
```

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/1b0d1c94-35ee-4869-b27a-4980647a7933)

* Create a new component called Message

* Message.tsx
  
```javascript
export default function Message() {
  return <div>Click here to get a message</div>;
}
```
* App.tsx

```javascript
import Message from "./components/Message";

function App() {
  return (
    <div className="App">
      <Message />
    </div>
  );
}

export default App;

```
  
  
