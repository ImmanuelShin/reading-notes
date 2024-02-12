# Class 27

## Django Models

Django models serve the purpose of defining the data structure and managing the database schema in a Django application. The basic structure involves creating a Python class for each model, where each class represents a database table. Model fields define the data types, relationships, and constraints. Models facilitate the creation, retrieval, updating, and deletion (CRUD) operations, making it easier to interact with the database. By using models, developers can abstract database interactions and maintain a high level of consistency and integrity in the application's data.

## Django Admin Interface

The Django Admin interface provides an out-of-the-box solution for managing the application's database records. Key features include a user-friendly interface for CRUD operations on models, automatic form generation, and a powerful search and filtering system. To customize the Django Admin interface, developers can create a custom admin.py file and define ModelAdmin classes. These classes allow customization of display fields, list filters, search fields, and more. By extending and modifying the default behavior, the Django Admin interface can be tailored to meet the specific needs and branding of a project.

## Key Components and Workflow

### Components:
1. **Models:** Define data structure and interact with the database.
2. **Views:** Handle user interactions, process requests, and return responses.
3. **Templates:** Define the presentation layer and generate dynamic HTML.
4. **URL Patterns:** Map URLs to corresponding views.
5. **Settings:** Configure the Django application.

### Workflow:
1. **User sends a request:** Triggered by a URL, it is directed to the corresponding view.
2. **View processes the request:** Interacts with models, performs business logic, and communicates with templates.
3. **Template generates HTML:** Dynamically incorporates data from the view.
4. **Response sent to the user:** HTML is rendered and sent back to the user.

## Things I want to know more about