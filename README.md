## 1. What is JSX, and why is it used?

**Ans:** JSX stands for JavaScript XML, a syntax extension for JavaScript. It allows you to write HTML-like code directly in your JavaScript files, and is primarily used with React to build user interfaces.

JSX is used because it makes coding a UI design much easier to write and read. We can create separate components for different parts of a design and connect them within a main file. You can also pass data between these components using props, which makes data management simple. This makes our code more intuitive and helps prevent common security issues like Cross-Site Scripting (XSS).

---

## 2. What is the difference between State and Props?

**Ans:**  

**State:** When we need to handle dynamic data in a component, we use state. State can store data and also update it according to user interactions. For example: counter, form inputs, API data, etc.

**Props:** On the other hand, props means “properties.” Using props, we can pass data from a parent component to a child component. But we cannot change data through props because they are read-only.

---

## 3. What is the useState hook, and how does it work?

**Ans:** The useState hook lets functional components in React store and manage dynamic data.  
It returns a state variable and a function to update that variable, causing the component to re-render when the state changes.  
useState works by returning an array with two items: the current state value and a function to update it.  
When you call the update function, React changes the state and automatically re-renders the component with the new value.

---

## 4. How can you share state between components in React?

**Ans:** Here is an example:

```
function Parent() {
  const [count, setCount] = useState(0);
  return (
    <>
      <Countercompo count={count} setCount={setCount} />
    </>
  );
}
```
Here, the state is declared using useState. The count holds the value 0 initially, and setCount is a function to update that state. Then, count and setCount are passed as props to the <Countercompo /> component. Inside <Countercompo />, these props can be received using destructuring.This way, the state of one component can be shared with another component and also used or updated there.

## 5. How is event handling done in React?
**Ans:** In React, event handling is done using camelCase syntax for event names and by passing a function as the event handler.

Example:

```
function Button() {
  function handleClick() {
    alert("Button clicked!");
  }

  return (
    <button onClick={handleClick}>
      Click Me
    </button>
  );
}
```


In this Button component, I created a button and set a click event on it. Then I declared a function named handleClick. Inside this function, I set an alert. When someone clicks the button, the alert will be shown.
