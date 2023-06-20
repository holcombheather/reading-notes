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
