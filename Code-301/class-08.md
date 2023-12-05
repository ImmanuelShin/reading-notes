# Class 08

## API

### API Design and Best Practices

Roy Fielding came up with Representational State Transfer (REST) in 2000 as an architectural approach to designing web services.
REST main principles:

- REST APIs are designed around resources.
  - Resources are any kind of data, object, or service that can be accessed by the client.
- A resource has an identifier.
  - Identifiers are URIs that uniquely identify that resource.
  - > https://order-food.com/orders/1
- REST APIs use a uniform interface, which helps decouple client/service implementation. HTTP APIs use standard HTTP verbs:
  - GET, POST, PUT, PATCH, DELETE.
- APIs use stateless request models. HTTP requests should be independent and can occur in any order.

When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations of the resource):
> https://order-food.com/orders (good)  
> https://order-food.com/create-order (bad)  

Also avoid using too complex URIs. Higher levels of complexity can be difficult to maintain and are inflexible to future resource relationship changes. Keeping URIs simple is a balancing act between denormalizing data and combining related information into bigger resources without fetching data the client doesn't need.

Status codes:

- GET:
  - 200: OK
  - 404: Not Found
- POST:
  - 201: Created
  - 400: Bad Request
- PUT:
  - 201: Created
  - 409: Conflict
- DELETE:
  - 204: No Content
  - 404: Not Found

## Things I want to know more about
