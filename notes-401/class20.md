# Component Based UI

**React Quick Start**

1. Building blocks of a React app: Components
2. HTML element vs React component: HTML elements are web page parts, React components are reusable, independent code pieces controlling UI.
3. JSX: JavaScript syntax extension allowing HTML in React for improved readability.
4. Embedding JavaScript in JSX: Use curly braces `{}`.
5. Special features for iteration/conditional logic: Use regular JavaScript, but React supports `.map()` for lists, ternary or short-circuit operators for conditions.
6. React's response to user inputs: Through synthetic events.
7. Word indicating Hook usage: "use" (like `useState`, `useEffect`).
8. Data sharing between components: Via props, Context, or state management libraries (Redux, MobX).

**Render and Commit**

1. Refreshing a React UI: Reconciliation, Rendering, Committing to DOM.
2. Trigger updates after initial render: Change state or props.
3. React recreating DOM nodes on rerender: No, only updates necessary parts using Diffing algorithm.
4. Post DOM update: Browser paints changes to the screen.

**Additional Questions**

1. Airbnb React/JSX Style Guide conventions: 

    - Naming Conventions: 
        - Variables, Functions, Instances: Use camelCase. 
          - Example: `let myVariable = 'example'; function myFunction() {...}; let myInstance = new MyClass();`
        - Components: Use PascalCase. 
          - Example: `class MyComponent extends React.Component {...}`
        - Filenames: Use appropriate extensions (.jsx for JSX files).
          - Example: `MyComponent.jsx`

    - Component Structure: 
        - Keep components small and functional where possible.
            - Example: `const MyComponent = (props) => {...}`

    - Type Checking: 
        - Use PropTypes for type checking. 
          - Example: `MyComponent.propTypes = {myProp: PropTypes.string.isRequired};`

    - JSX Attributes: 
        - Always use double quotes for JSX attributes.
            - Example: `<div className="myClass"></div>`

    - Keys in Lists: 
        - Avoid using array indexes for keys.
            - Example: `myArray.map((item, index) => <li key={item.id}>{item.name}</li>)`

2. Looking ahead at this module’s course schedule, What do you look forward to learning?
    - Hooks 
3. What are your learning goals after reading and reviewing the class README?
    - **Describe and Define**: 
        - Understand and explain concepts such as SASS - Nesting and Variables, “Component Architecture”, Application and Component “State”, and the difference between Libraries and Frameworks. 
        - Understand the basics of a React App including its structure and key elements such as index.html, index.js, the role of JSX, the concept of components (both class and function-based), and component interactions.

    - **Execute**: 
        - Develop practical skills such as creating a React project locally with create-react-app, using codesandbox.io to work live on a React application, creating and rendering Class and Functional React components to the DOM.
        - Learn to add event listeners to React components, update React component state, and style React applications/components using SASS.

***

## Class 20 Lecture Notes

- What is SASS? 

    SASS, which stands for Syntactically Awesome Stylesheets, is a preprocessor scripting language that is interpreted or compiled into Cascading Style Sheets (CSS). 

    It provides a more advanced and efficient way to write CSS and introduces features like variables, nested rules, mixins, functions, and inheritance, which are not available in pure CSS. This allows for code to be more reusable and manageable, particularly in larger projects. 

    For example, SASS allows for variables, which can simplify the task of changing color schemes or other common properties. If you decide to change a color, instead of having to manually update every reference to that color in your CSS, you can just change the value of the variable in one place.

    Here's a simple example of how you might use a variable in SASS:

    ```scss
    $primary-color: #3cb44b;

    body {
    background-color: $primary-color;
    }
    ```

    The above SASS code compiles into the following CSS:

    ```css
    body {
    background-color: #3cb44b;
    }
    ```

    In addition to the SCSS syntax (Sassy CSS) that is similar to CSS, SASS also includes an indented syntax (often simply called "SASS") that uses indentation to separate code blocks and newline characters to separate rules.


- What is state? 

    In the context of React, "state" is a built-in object that a component can use to store property values that belong to that component. When the state object changes, the component re-renders, meaning it updates the DOM to reflect the new state.

    State is typically used to store information that should be persistently tracked and dynamically changed throughout the lifecycle of the component. This might include user inputs, form data, or data fetched from an API.

    Here is an example of state in a functional component using the `useState` hook:

    ```jsx
    import React, { useState } from 'react';

    function ExampleComponent() {
    // Declare a new state variable, which we'll call "count"
    const [count, setCount] = useState(0);

    return (
        <div>
        <p>You clicked {count} times</p>
        <button onClick={() => setCount(count + 1)}>
            Click me
        </button>
        </div>
    );
    }
    ```

    In this example, `useState` is a Hook that lets you add React state to function components. `useState` returns a pair of values: the current state and a function that updates it. In the above example, `count` is the current state, `setCount` is the function to update it, and `useState(0)` means that the initial state value is 0. 

    When the user clicks the button, it triggers the `setCount` function, which updates the state, and causes the component to re-render with the updated state.

- Difference between framework and library? 

    Libraries and frameworks are both reusable code written by someone else that helps you develop your own applications more quickly and efficiently. They both provide pre-written code for common tasks to help speed up development. However, they have different ways of controlling the flow of code execution.

    1. **Library**: A library is a collection of functions and methods that you can call to perform specific tasks. Libraries don't dictate how your application is structured or how it should work. They simply provide functionality that you can use within your application as needed. When you use a library, you are in charge of the flow of the application, and you decide when and where to use the library. Examples of libraries include Lodash, Moment, or React.

    2. **Framework**: A framework, on the other hand, provides a structure for your application. It dictates how your application should be structured and how it should work. The framework is in charge of the flow, and it provides places for you to plug in your own code, but it calls your code rather than the other way around. This is often referred to as "Inversion of Control". When you use a framework, you have to follow its rules and structure. Examples of frameworks include Angular, Vue.js, or Django.

    In summary, the main difference between a library and a framework is "Inversion of Control". When you call a method from a library, you are in control. But with a framework, the control is inverted: the framework calls you.

- Basics of React

    1. **Basics of a React App**: A React application is built out of components, which are JavaScript classes or functions that optionally accept inputs, or "props", and return a React element that describes how a section of the UI should appear.

    2. **index.html in public (root div)**: This is the main HTML file for your application. It contains a div with the id "root", which is the entry point for your React application. React will inject your components into this div for rendering to the DOM.

    3. **index.js as an untouchable “bootstrap” or “entry point”**: The index.js file is the main entry point to your React application. It is where your root React component (often named `App`) gets rendered to the root div in your index.html file. Typically, you don't make a lot of changes to this file except to wrap your App component in any context providers that you're using.

    4. **React Renders into that div**: React controls the content of the root div in index.html by rendering a React component into it. This is done by using `ReactDOM.render()`. The specified component and its child components become the content of the div.

    5. **JSX is actually JavaScript but it looks like markup**: JSX is a syntax extension for JavaScript that allows you to write HTML-like syntax in your JavaScript code. It's used for defining the structure of components in React. Under the hood, it's transformed into regular JavaScript calls to React's `React.createElement()` function.

    6. **Components can be classes or functions. What gets “returned” gets “rendered”**: React components can be defined as classes or functions. In either case, they return what's called "JSX", which is then rendered to the DOM by React. For class components, the `render` method returns the JSX. For function components, the function itself returns the JSX.

    7. **Class - render() { return(jsx) }**: In a class component, the `render` method is used to specify what the UI should look like. The `render` method returns JSX.

    8. **Function - return(jsx)**: Function components are simpler than class components. They're just JavaScript functions that return JSX.

    9. **Components can load and render each other**: React components can import and use other components, just like JavaScript modules can import functions from other modules. This allows you to build complex UIs out of simple components.

    10. **Components can load their own CSS**: Each React component can import its own CSS file, which means that the styles for a component are defined and maintained with the component itself. This makes components more self-contained and reusable.

- What is the difference between a unit test and an integration test? 

    1. **Unit Test**: A unit test is focused on testing individual "units" of code in isolation from the rest of the system. A unit could be a function, method, or class. The goal is to verify that each unit of the code performs as expected. For example, given specific inputs to a function, you might check whether the function returns the expected output. Unit tests should be isolated, meaning they shouldn't depend on any external factors such as a database or network. Any dependencies for the unit under test are usually "mocked" or "stubbed" to ensure that the tests only evaluate the functionality of the unit itself.

    2. **Integration Test**: Integration tests, on the other hand, check how different units of the system work together. They are designed to catch issues that might arise when different components interact, such as data inconsistencies, communication problems, or incorrect behavior. For example, you might have an integration test that checks whether a button in the UI correctly calls a certain function and updates the application state. In contrast to unit tests, integration tests typically do interact with external systems like databases or networks.

    In summary, while unit tests are concerned with the functionality of individual pieces of a system, integration tests are concerned with the functionality of the system as a whole, or at least the interaction between its different pieces.
