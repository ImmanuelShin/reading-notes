# Class 28

## Django Forms

Django Forms play a crucial role in handling user input by providing a structured way to define, validate, and process user-submitted data. Key components of creating a form using the Django framework include:

### Displaying the Form

- When a user requests a page containing a form, Django displays the default form.
- The form may be unbound (not associated with user-entered data) and can have blank fields for new records or pre-populated with initial values for record modification.

### Receiving and Binding Data

- Upon receiving a submit request, Django binds the data to the form.
- Data binding means that user-entered data and any errors are associated with the form, allowing easy retrieval.

### Cleaning and Validating Data

- Data cleaning involves sanitizing input fields, removing invalid characters, and converting them into consistent Python types.
- Validation checks ensure that the entered values are appropriate for each field (e.g., within the correct date range, proper length).
- If any data is invalid, the form is redisplayed with user-populated values and error messages for the problematic fields.

### Performing Required Actions

- If all data is valid, Django performs the required actions, such as saving data, sending emails, executing search results, or handling file uploads.
- Actions depend on the specific use case of the form.

### Redirecting the User

- After completing all actions, Django redirects the user to another page.
- This helps maintain a clean and understandable user experience.

Django simplifies the form handling process through the use of the Form class. The Form class facilitates the generation of HTML for forms and simplifies data cleaning and validation. Understanding how the Form class is used is essential for working with Django's higher-level form framework classes.

## Templates and Template Inheritance

Django templates play a pivotal role in structuring the layout and content of web pages. Template inheritance, a powerful feature, enhances code reusability and maintainability.

### Defining URLs and Components
- URL mappers forward supported URLs to view functions.
- View functions retrieve data from models and create HTML pages for user display.
- Templates define the structure and layout of HTML pages.

### Template Inheritance

- Templates can be extended to create a base template with common elements.
- The `extends` template tag is used to specify the base template.
- Sections in the base template are marked with `block` and `endblock` tags for dynamic content.

### Base Template Example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    {% blockquote %}
      <title>Local Library</title>
    {% endblockquote %}
    <!-- Additional head content -->
  </head>
  <body>
    {% blockquote %}
      <!-- Default navigation content -->
    {% endblockquote %}
    {% blockquote %}
      <!-- Default content -->
    {% endblockquote %}
  </body>
</html>
```

### Extending Base

```html
{% extends "base_generic.html" %}

{% blockquote %}
  <h1>Local Library Home</h1>
  <p>
    Welcome to LocalLibrary, a website developed by
    <em>Mozilla Developer Network</em>!
  </p>
  <!-- Additional dynamic content -->
{% endblockquote %}
```

## Referencing Static Files

The `{% load static %}` tag enables referencing static files like CSS and images. URLs for static files are specified using the `static` template tag.

## Linking to URLs

The `url` template tag generates URLs based on path functions in `urls.py`. This improves flexibility and avoids hardcoding URLs.

## Configuring Template Locations

The `TEMPLATES` object in `settings.py` specifies template configuration. `'APP_DIRS': True` directs Django to search for templates in each application's "templates" subdirectory.

## Views

In Django, views handle HTTP requests and return HTTP responses. The primary function of a view is to process the user's request, interact with the database or other data sources, and generate an appropriate response, typically in the form of an HTML page. Views play a crucial role in implementing the application's logic and determining how data is presented to the user.

When a user makes an HTTP request to a Django application, the request is directed to a specific view, which processes the request and generates an appropriate response. Views can perform various tasks, including querying the database, handling form submissions, and rendering templates to display information.

### Function-Based Views (FBVs)

- **Definition:** Function-Based Views are defined as Python functions.
- **Simplicity:** FBVs are simpler and more straightforward, making them easier to understand, especially for smaller projects.
- **Procedural:** FBVs follow a procedural programming approach, and each view function typically handles a specific type of request.
- **Flexibility:** They provide more flexibility in terms of control flow and logic.

```python
from django.shortcuts import render

def my_view(request):
    # View logic here
    return render(request, 'template.html', context)
```

### Class-Based Views (CBVs)

- **Definition:**: Class-Based Views are defined as Python classes.
- **Organization**: CBVs offer a more organized structure, particularly for larger projects, by grouping related functionality into classes.
- **Reusability**: They encourage code reuse through inheritance and mixins, making it easier to extend and customize views.
- **Object-Oriented**: CBVs follow an object-oriented programming approach, providing a clear separation of concerns.

```python
from django.views import View
from django.shortcuts import render

class MyView(View):
    def get(self, request):
        # View logic here
        return render(request, 'template.html', context)
```

### Built-in Views

- CBVs provide built-in generic views: Django includes a set of generic class-based views (e.g., DetailView, ListView) that encapsulate common patterns, reducing the amount of code needed for standard operations.
- Mixin Classes: Mixins can be used with CBVs to extend functionality without the need for rewriting the entire view.

```python
from django.views.generic import ListView

class MyListView(ListView):
    model = MyModel
    template_name = 'my_template.html'
    context_object_name = 'my_objects'
```

## Things I want to know more about
