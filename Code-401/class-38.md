# Class 38

## React

### Conditional Rendering

Conditional rendering in React allows components to show different content based on certain conditions. This is achieved through the use of conditional statements within the component's render method.

```jsx
class ConditionalRenderingExample extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      isLoggedIn: true,
    };
  }

  render() {
    return (
      <div>
        {this.state.isLoggedIn ? (
          <p>Welcome, User!</p>
        ) : (
          <p>Please log in to continue.</p>
        )}
      </div>
    );
  }
}
```

### Lists & Keys

Lists are commonly used in React to render a collection of items dynamically. When rendering lists, it's important to assign a unique "key" to each item to help React efficiently update and re-render the list when changes occur.

```jsx
class ListExample extends React.Component {
  render() {
    const items = ['Item 1', 'Item 2', 'Item 3'];

    return (
      <ul>
        {items.map((item, index) => (
          <li key={index}>{item}</li>
        ))}
      </ul>
    );
  }
}
```

### Forms

In React, forms are used to handle user input. React provides a controlled component approach, where form elements are controlled by React state. This allows for easy handling of form data and validation.

```jsx
class FormExample extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      username: '',
      password: '',
    };
  }

  handleChange = (e) => {
    this.setState({ [e.target.name]: e.target.value });
  };

  handleSubmit = (e) => {
    e.preventDefault();
  };

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <input
          type="text"
          name="username"
          value={this.state.username}
          onChange={this.handleChange}
        />
        <input
          type="password"
          name="password"
          value={this.state.password}
          onChange={this.handleChange}
        />
        <button type="submit">Submit</button>
      </form>
    );
  }
}
```

### Lifting State

Lifting State in React involves moving the state of a component up to a common ancestor. This is useful when multiple components need to share and synchronize the same state.

```jsx
class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      sharedState: '',
    };
  }

  updateState = (newState) => {
    this.setState({ sharedState: newState });
  };

  render() {
    return (
      <div>
        <ChildComponent onUpdate={this.updateState} />
        <AnotherChildComponent sharedState={this.state.sharedState} />
      </div>
    );
  }
}

class ChildComponent extends React.Component {
  handleChange = (e) => {
    this.props.onUpdate(e.target.value);
  };

  render() {
    return <input type="text" onChange={this.handleChange} />;
  }
}
```

### Composition vs Inheritance

In React, composition and inheritance are two ways to reuse component code. Composition involves using components as building blocks, combining them to create more complex components. Inheritance, on the other hand, involves creating a new component that extends the functionality of an existing component.

```jsx
const Header = ({ title }) => <h1>{title}</h1>;

const Content = ({ text }) => <p>{text}</p>;

const Page = ({ title, content }) => (
  <div>
    <Header title={title} />
    <Content text={content} />
  </div>
);
```
```jsx
class Animal {
  makeSound() {
    console.log('Generic Animal Sound');
  }
}

class Dog extends Animal {
  makeSound() {
    console.log('Bark');
  }
}
```

## Thinking in React

### Start with the mockup

- Begin with a mockup or design provided by a designer.
- Imagine having a JSON API that returns data in a structured format.

### Break the UI into a component hierarchy

- Identify and name components based on the mockup.
- Use principles from programming, CSS, and design to decide how to split the design into components.
- Components should match the shape of the data model.

### Build a static version in React

- Create a static version of the app that renders the UI without any interactivity.
- Build reusable components that represent the data model.
- Establish one-way data flow, passing data from top-level components to the ones at the bottom.

### Find the minimal but complete representation of UI state

- Identify the minimal set of changing data (state) needed for interactivity.
- Distinguish between state and non-state data.
- Keep the state DRY (Don't Repeat Yourself).

### Identify where your state should live

- Determine which component should own and manage each piece of state.
- Follow the one-way data flow principle in React.
- Use common parent components to hold shared state.

### Add inverse data flow

- Make the UI interactive by supporting data flow from form components to the state.
- Pass down state-changing functions as props to child components.
- Implement event handlers in child components to update the state in parent components.

The methodology encourages the creation of a clear component hierarchy, promotes the separation of concerns, and helps manage state in a structured way. It emphasizes the importance of thinking about the structure of the application before diving into the coding phase, leading to more maintainable and scalable React applications.

## Things I want to know more about

