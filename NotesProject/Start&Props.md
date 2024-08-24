# React.js: Understanding Props and State

## What are Props?
Props (short for "properties") are read-only attributes used to pass data from one component to another in React. They allow components to be reusable by making them configurable and dynamic. Props are passed from parent to child components and cannot be modified by the child.

## State vs. Props [Comparison Table]

| Feature       | State                                                    | Props                                                              |
|---------------|----------------------------------------------------------|--------------------------------------------------------------------|
| **Definition** | Represents the dynamic data of a component that can change over time | Read-only attributes used to pass data from one component to another |
| **Mutability** | Mutable, can be updated using `setState()`                | Immutable, cannot be changed by the receiving component            |
| **Usage**      | Used for data that changes over time and affects rendering | Used to pass data and event handlers to child components           |
| **Initialization** | Initialized within the component                         | Passed to the component from outside (usually from a parent component) |
| **Accessibility** | Accessible within the component where it is defined       | Accessible only in the component where they are passed             |
| **Lifecycle**  | Can change over time within the component                  | Remains constant during the component's lifecycle                  |
| **Example**    | Form input values, toggles, counters                       | Component title, theme, event handlers                             |

## Difference Between State and Props in React.js
State is a local data storage that is specific to a component and can be changed over time. It represents the dynamic aspects of the component and determines the component's behavior and rendering.  
Props are external data passed into a component from its parent and cannot be changed by the component itself. They are used to configure and customize the component's output.

## How are Props Passed into the Component?
Props are passed into a component as attributes in JSX. For example:

```jsx
function ChildComponent(props) {
  return <div>{props.name}</div>;
}

function ParentComponent() {
  return <ChildComponent name="John" />;
}
