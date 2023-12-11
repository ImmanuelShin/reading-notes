# Class 12

## CRUD

### Status Codes

HTTP defines multiple status codes. These codes are typically grouped into categories depending on what the code represents.

- 100's: Informational - Tells the client that the request has been received.
- 200's: Success - Tells the client that the request has been accepted.
  - 202: Request was valid, but the processing will finish at a later time.
  - 204: No Content - Can be used for update requests that don't return data to the client.
- 300's: Redirection code - Tells the client that the requested resource isn't available anymore.
  - 308: Permanent Redirect - If the resource is at another URL and should be accessed at that URL for the foreseeable future.
- 400's: Client error - Invalid requests made by the client to the server.
  - 403: Forbidden - Client doesn't have permission to access resource regardless of authorization.
- 500's: Server error - Problems by dysfunctional/overwhelmed/unreachable servers.

## REST API with MongoDB

Creating a REST API has a few steps and a few notes of advice.

When connecting to our MongoDB, we want to pull from our .env file. We do this for security, probably.

Middleware is also useful to keep our server files modulated and clean. Middleware connects the main file to individual middleware functions that are external modules containing various functions to handle different HTTP requests.  
We write app.use(express.json()) in order to use any middleware that we create.

When writing out our routes, we can use /:variable, where ':' signifies a parameter, and the variable name represents the specific parameter name accepted.  

PUT updates all the information whereas PATCH only updates specific items passed through.

When interacting with our database, we need to define a model. This model determines how we interact with the database. In our model, we need to create schemas. These schemas show what data and what types of data are being searched for.

In case our database can't find any data, we send a 500 error. This represents an error on the server side and not the client.

In the case that the client is creating a new entry, we can send a 201 code. This sends a message to the client saying that the object was successfully created. This is preferred over 200, or a generic success message, because it more specifically matches our success status.

## Things I want to know more about
