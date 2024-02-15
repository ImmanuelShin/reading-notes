# Class 31

## Docker 

Docker is a platform for developing, shipping, and running applications in lightweight, portable containers. Containers encapsulate the application, its dependencies, and runtime environment, ensuring consistency across different computing environments and facilitating efficient deployment and scaling.

Docker containers consist of the following key components:

1. **Images:** Snapshots of a file system and application code, along with metadata.
2. **Containers:** Running instances of Docker images, isolated from the host system.
3. **Dockerfile:** A script defining steps to create a Docker image.
4. **Registry:** A repository for sharing and storing Docker images.
5. **Docker Engine:** The runtime that manages containers on a host system.

Docker containers streamline development and deployment by providing consistency across different environments, facilitating easy scaling, and enabling efficient resource utilization.

## Building a Library Website with Django

1. **Models:** Define data models for books, authors, and other entities in `models.py`.
2. **Views:** Implement views to handle user requests and interact with models in `views.py`.
3. **Templates:** Create HTML templates in the `templates` directory to render dynamic content.

Example of a model in `models.py`:

```python
from django.db import models

class Book(models.Model):
    title = models.CharField(max_length=100)
    author = models.ForeignKey('Author', on_delete=models.CASCADE)

class Author(models.Model):
    name = models.CharField(max_length=50)
    bio = models.TextField()
```

Example of a view in views.py:

```python
from django.shortcuts import render
from .models import Book

def book_list(request):
    books = Book.objects.all()
    return render(request, 'library/book_list.html', {'books': books})
```

## Django vs. Django REST framework

- **Django:**
  - Primarily used for building web applications.
  - Emphasizes the Model-View-Controller (MVC) architectural pattern.
  - Provides an ORM (Object-Relational Mapping) for database interaction.
  - Uses regular Django views for handling HTTP requests.

- **Django REST framework:**
  - Specialized for building Web APIs.
  - Follows the Model-View-Template (MVT) pattern.
  - Offers serializers for transforming complex data types, like querysets, into native Python datatypes for easy rendering to JSON or XML.
  - Utilizes class-based views specifically designed for handling API requests.

## Things I want to know more about