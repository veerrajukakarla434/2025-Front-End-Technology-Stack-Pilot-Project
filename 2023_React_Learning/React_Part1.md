# 2023 React Learning

#### ReactJs Basics 

* **Reasons to learn ReactJS**
* React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It is a Model-View-Controller (MVC) architecture-based library that plays the role of “V” which means view. It designs simple views for each state in your application, and React will efficiently update and render just the right component when your data changes. The declarative view makes your code more predictable and easier to debug.

* **Top 5 Reasons to Learn React JS in 2023**
  * Ref: https://dev.to/alterclass/5-reasons-why-you-should-learn-react-js-2jfc
  * Ref: https://www.knowledgehut.com/blog/web-development/reasons-to-learn-reactjs
  * Ref : https://medium.com/@SilentHackz/top-10-reasons-why-you-should-learn-react-right-now-f7b0add7ec0d
* **Prerequisite:**
* Before you start learning ReactJS, we assume that you have knowledge of HTML, CSS and JavaScript. There are few others skill sets that will help you to complete this tutorial at your best pace.

####  **React Features:**

* **Use JSX:** JSX is faster than normal JavaScript as it performs optimizations while translating to regular JavaScript. It makes it easier for us to create templates.

* **Virtual DOM:** Virtual DOM exists which is like a lightweight copy of the actual DOM. So for every object that exists in the original DOM, there is an object for that in React Virtual DOM. It is exactly the same, but it does not have the power to directly change the layout of the document. Manipulating DOM is slow, but manipulating Virtual DOM is fast as nothing gets drawn on the screen.

* **One-way Data Binding:** One-way data binding gives you better view over your application.

* **Component:** A Component is one of the core building blocks of React. In other words, we can say that every application you will develop in React will be made up of pieces called components. Components make the task of building UIs much easier.

* **Performance:** ReactJS use JSX, which is faster compared to normal JavaScript and HTML. Virtual DOM is a less time taking procedure to update webpages content.

#### ReactJS Data Binding

* Data Binding is the process of connecting the view element or user interface, with the data which populates it.

* In **ReactJS**, components are rendered to the user interface and the component’s logic contains the data to be displayed in the view(UI). The connection between the data to be displayed in the view and the component’s logic is called data binding in ReactJS.

* **One-way Data Binding:** ReactJS uses one-way data binding. In one-way data binding one of the following conditions can be followed:

* **Component to View:** Any change in component data would get reflected in the view.
* **View to Component:** Any change in View would get reflected in the component’s data.

#### ReactJS Virtual DOM

* **What is DOM?**
* DOM stands for ‘Document Object Model’. In simple terms, it is a structured representation of the HTML elements that are present in a webpage or web app. DOM represents the entire UI of your application. The DOM is represented as a tree data structure. It contains a node for each UI element present in the web document. It is very useful as it allows web developers to modify content through JavaScript, also it being in structured format helps a lot as we can choose specific targets and all the code becomes much easier to work with.

* **Disadvantages of real DOM?**
* Every time DOM gets updated, the updated element and its children have to be rendered again to update the UI of our page. For this, each time there is a component update, the DOM needs to be updated and the UI components have to be re-rendered.
Example: 
```java
// Simple getElementById() method
document.getElementById('some-id').innerValue = 'updated value';
```
* **What is Virtual DOM?**
* React uses Virtual DOM exists which is like a lightweight copy of the actual DOM(a virtual representation of the DOM). So for every object that exists in the original DOM, there is an object for that in React Virtual DOM. It is exactly the same, but it does not have the power to directly change the layout of the document. 

* **Manipulating DOM is slow, but manipulating Virtual DOM is fast** as nothing gets drawn on the screen. So each time there is a change in the state of our application, the virtual DOM gets updated first instead of the real DOM. 

* **How does virtual DOM actually make things faster?**
* When anything new is added to the application, a virtual DOM is created and it is represented as a tree. Each element in the application is a node in this tree. So, whenever there is a change in the state of any element, a new Virtual DOM tree is created. This new Virtual DOM tree is then compared with the previous Virtual DOM tree and make a note of the changes. After this, it finds the best possible ways to make these changes to the real DOM. Now only the updated elements will get rendered on the page again.

* **How virtual DOM Helps React?**
In React, everything is treated as a component be it a functional component or class component. A component can contain a state. Whenever the state of any component is changed react updates its Virtual DOM tree. Though it may sound like it is ineffective the cost is not much significant as updating the virtual DOM doesn’t take much time. 

* React maintains two Virtual DOM at each time, one contains the updated Virtual DOM and one which is just the pre-update version of this updated Virtual DOM. Now it compares the pre-update version with the updated Virtual DOM and figures out what exactly has changed in the DOM like which components have been changed. This process of comparing the current Virtual DOM tree with the previous one is known as ‘diffing’. Once React finds out what exactly has changed then it updates those objects only, on real DOM. 

* React uses something called batch updates to update the real DOM. It just means that the changes to the real DOM are sent in batches instead of sending any update for a single change in the state of a component. 

* We have seen that the re-rendering of the UI is the most expensive part and React manages to do this most efficiently by ensuring that the Real DOM receives batch updates to re-render the UI. This entire process of transforming changes to the real DOM is called Reconciliation.

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/d6f1104e-1ca0-43cc-967d-8b35e0b33507)

#### ReactJS Reconciliation

* The reconciliation process makes React work faster. **Reconciliation** is the process through which React updates the Browser DOM.

* Important concepts behind the **working of the Reconciliation process** are:

* **Virtual DOM**  
* **Diffing Algorithm**

* The term **rendering in React** can closely be identified as **making** or **becoming**. In traditional rendering, Browser does the following tasks:

* Creates a DOM (Document Object Model) represented by a tree structure.
* Renders any new data to the DOM even if data is similar to previous ones.
* This rendering by Browser has a sequence of steps and is rather costly in nature. The concept of Virtual DOM used by React makes rendering much faster.

* **Virtual DOM:** React renders JSX components to the Browser DOM, but keeps a copy of the actual DOM to itself. This **copy** is the **Virtual DOM**. We can think of it as the twin brother of the real or Browser DOM. The following actions take place in React:

* React **stores a copy of Browser DOM** which is called **Virtual DOM**.
* When we **make changes or add data,** React creates a **new Virtual DOM** and **compares it with the previous** one.
* **Comparison** is done by **Diffing Algorithm**. The cool fact is all these comparisons **take place in the memory** and nothing is yet changed in the Browser.
* After comparing, React goes ahead and creates a **new Virtual DOM having the changes.** It is to note that as many as 200,000 virtual DOM nodes can be produced in a second.
* Then it **updates the Browser DOM** with the **least number of changes** possible **without rendering the entire DOM** again. (Ref: Fig.1) This changes the efficiency of an application tremendously

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/5eef820c-ea8b-4616-816b-469e752f1c8c)


* Suppose we have new data similar to the previous one, Virtual DOM compares previous and new structures and sees that it has no change, so nothing gets rendered to the Browser. This is how the Virtual DOM is helping to enhance the Browser performance.

