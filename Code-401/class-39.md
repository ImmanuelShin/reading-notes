# Class 39

## React Context

React Context is a feature in React that provides a way to pass data through the component tree without having to pass props manually at every level. It facilitates state management and data sharing in React applications, especially in scenarios where multiple components need access to the same data.

- **Key Components:**
  - **`createContext` function:**
    - Creates a Context object that includes a `Provider` and a `Consumer`.

  - **`<Context.Provider>`:**
    - Wraps the part of the component tree where the data needs to be made available.
    - Accepts a `value` prop, which is the data to be shared.

  - **`<Context.Consumer>`:**
    - Consumes the data provided by the `Provider`.
    - Renders a function with the shared data as an argument.

## useContext

A React hook that allows functional components to consume data from a React Context without the need for a `Context.Consumer` component.

- **Usage:**
  - **Import:**
    ```jsx
    import React, { useContext } from 'react';
    ```

  - **Accessing Data:**
    ```jsx
    const MyComponent = () => {
      const contextData = useContext(MyContext);
    };
    ```

  - **Parameters:**
    - `useContext` takes a Context object as its argument.

  - **Return Value:**
    - Returns the current context value for the given Context.

## Next.js

A React framework for building modern web applications. It aims to simplify and streamline the development process by providing a set of conventions and tools, enabling developers to build scalable and optimized applications.

Example with MongoDB:
- **Setup:**
  - Execute the following commands to bootstrap the example:
    ```bash
    npx create-next-app --example with-mongodb with-mongodb-app
    ```

- **Configuration:**
  - Set up a MongoDB database, either locally or with MongoDB Atlas.
  - Copy `.env.local.example` to `.env.local` and set the `MONGODB_URI` variable with your connection string.

- **Development:**
  - Run Next.js in development mode:
    ```bash
    npm install
    npm run dev
    ```
  - Access the app at http://localhost:3000.

- **Deployment:**
  - Deploy the app on Vercel using the provided deployment options.
  - Ensure to set environment variables on Vercel matching the ones in `.env.local`.

## Things I want to know more about