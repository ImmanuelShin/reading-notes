# Class 26

## Key Components of Django Framework

Django framework comprises several key components that collectively contribute to building web applications:

- **Models:** Represent the data structure and define the database schema.
- **Views:** Handle user interactions, process requests, and return appropriate responses.
- **Templates:** Define the presentation layer, allowing the dynamic generation of HTML.

These components work together to enforce the "Don't Repeat Yourself" (DRY) principle and facilitate rapid development by providing a structured and organized approach.

## Django’s MTV Architecture and Web Request-Response Cycle

Django's MTV (Model-View-Template) architecture divides the application into three main components:

- **Model:** Represents the data structure and manages interactions with the database.
- **View:** Handles user interactions, processes requests, and communicates with the model and template.
- **Template:** Defines the presentation layer, allowing the dynamic generation of HTML.

In a typical web request-response cycle, the following steps occur:
1. The user sends a request to the Django application.
2. The URL patterns direct the request to the corresponding view.
3. The view interacts with the model to fetch or manipulate data.
4. The template renders the dynamic HTML, incorporating data from the view.
5. The response is sent back to the user.

This separation of concerns in MTV enhances modularity, maintainability, and code organization.

## Purpose of Tailwind CSS and Differences from Bootstrap CSS

- **Tailwind CSS:** A utility-first CSS framework that focuses on providing low-level utility classes to build designs directly in the markup. It offers flexibility and customization without predefined components.
- **Purpose:** Tailwind CSS aims to provide a more granular and customizable approach to styling, allowing developers to create unique designs without being tied to pre-designed components.

### Differences from Bootstrap CSS

1. **Approach:** Tailwind is utility-first, while Bootstrap is component-first.
2. **Customization:** Tailwind allows more fine-grained customization, while Bootstrap offers a predefined set of components with limited flexibility.
3. **File Size:** Tailwind generates smaller CSS files as only the used utilities are included, reducing the overall file size compared to Bootstrap's comprehensive styling.

In summary, Tailwind CSS provides a more flexible and customizable styling approach compared to the component-driven structure of Bootstrap CSS.

## Things I want to know more about
