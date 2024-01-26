# Class 16

## Serverless Computing

Serverless is a cloud model that allows developers to build and run code without the need for managing backend infrastructure.  
It allows developers to not have to worry about server side code and put their all into making things look nice and run well.  
It doesn't remove servers entirely. It just outsources the servers to a different company.

## Vercel

An end-to-end platform for developers to more efficiently build and deploy web applications. It allows you to choose templates when creating projects and is essentialy a SquareSpace for developers.  
To get started: 

1. Use a template or import an existing project.
2. Add a domain.
3. Choose some customization options for your app.

# APIs

APIs are application programming interfaces. They act as a communication layer that allows for different systems to talk to eachother. Requests are made to the API and responses are given in the form of some sort of data or information.  
API calls usually follow common design models:

- SOAP (Simple Object Access Protocol) is typically associated with the enterprise world, has a stricter contract-based usage, and is mostly designed around actions.
- REST (Representational State Transfer) is typically used for public APIs and is ideal for fetching data from the Web. It’s much lighter and closer to the HTTP specification than SOAP.

Now, there's also GraphQL that is on the up and coming. 

### Calling

Calling APIs in Python requires the importing of certain libraries. A common one is the Requests library.

```
>>> import requests
>>> requests.get("https://randomuser.me/api/")
<Response [200]>
```

## Things I want to know more about
