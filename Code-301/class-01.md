# Class 01

## Introduction to React and Components

### Component-Based Architecture

"A component is a modular, portable, replaceable, and reusable set of well-defined functionality that encapsulates its implementation and exporting it as a higher-level interface."  
Components are objects that are meant to interact with other objects and represent the building blocks of component architecture.

They encapsulate these characteristics:

- Reusability: Components are usually designed to be reused in different situations in different applications. However, some components may be designed for a specific task.  
- Replaceable: Components may be freely substituted with other similar components.  
- Not context specific: Components are designed to operate in different environments and contexts.  
- Extensible: A component can be extended from existing components to provide new behavior.  
- Encapsulated:  A component depicts the interfaces, which allow the caller to use its functionality, and do not expose details of the internal processes or any internal variables or state.  
- Independent: Components are designed to have minimal dependencies on other components.  

Advantages that come from using components and component-based architecture:

- Ease of deployment: As new compatible versions become available, it is easier to replace existing versions with no impact on the other components or the system as a whole.  
- Reduced cost: The use of third-party components allows you to spread the cost of development and maintenance.  
- Ease of development: Components implement well-known interfaces to provide defined functionality, allowing development without impacting other parts of the system.  
- Reusable: The use of reusable components means that they can be used to spread the development and maintenance cost across several applications or systems.  
- Modification of technical complexity: A component modifies the complexity through the use of a component container and its services.  
- Reliability: The overall system reliability increases since the reliability of each individual component enhances the reliability of the whole system via reuse.  
- System maintenance and evolution: Easy to change and update the implementation without affecting the rest of the system.  
- Independent: Independency and flexible connectivity of components. Independent development of components by different group in parallel. Productivity for the software development and future software development.  

[source](https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm)

### Props in React

Props is a keyword used in React that stands for properties. It is used to pass data from one component to another.

It is important to remember that React passes data in a uni-directional flow. Prop data is also read-only, so data is passed down from parent to child only, and it should not be changed by the child, only read.

In order to use Props:

- We first define an attribute and its value.
- We then pass it to child components by using Props.
- We finally render the Props data.

[source](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0#:~:text=%E2%80%9CProps%E2%80%9D%20is%20a%20special%20keyword,way%20from%20parent%20to%20child)

## Things I want to know more about
