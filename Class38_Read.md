## How does lifting state up in a React application help with managing data flow and what are the benefits of using this approach?

### How?

Several components need to reflect the same changing data so the best way to do this is by lifting the shared state up to their closest common ancestor

### What?

**1. Single Source of Truth:** By lifting the state up, we create a "single source of truth" for our data. This means that instead of maintaining the same data in multiple components (which can lead to inconsistencies and bugs), we maintain it in one place. 

**2. Data Flow Control:** It becomes easier to track the data flow in our app. In React, data can be passed down the component tree via props, creating a unidirectional data flow.

**3. Enhanced Reusability:** Components that rely only on their props can be used in different parts of the app without needing to duplicate code or state, enhancing reusability.


## Explain the concept of conditional rendering in React and provide an example of how to implement it in a component.

### Concept:

In React, we can create distinct components that encapsulate the behavior we need. Then, we can render only some of them, depending on the state of your application. That's what Conditional Rendering 

### Example:

```
function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}

const root = ReactDOM.createRoot(document.getElementById('root')); 
// Try changing to isLoggedIn={true}:
root.render(<Greeting isLoggedIn={false} />);

```

## What are the main principles behind “Thinking in React” and how do they guide the process of designing and building a React application?


1. Break the UI into a component hierarchy 
2. Build a static version in React
3. Find the minimal but complete representation of UI state 
4. Identify where your state should live
5. Add inverse data flow




