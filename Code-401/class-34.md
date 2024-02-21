# Class 34

## Django Settings

Setting your django settings can prove difficult for a number of reasons: working with different environments, sensitive data, coordinating settings across multiple team members, etc. 

### Configuration Approaches

#### `settings_local.py` Approach

**Pros:**
- Secrets not in VCS.
  
**Cons:**
- `settings_local.py` is not in VCS, so you can lose some Django environment settings.
- The Django settings file is a Python code, so `settings_local.py` can have non-obvious logic.
- Need `settings_local.example` (in VCS) to share default Django configurations for developers.

#### Separate Settings File for Each Environment

**Pros:**
- All environments are in VCS.
- Easy to share settings between developers.

**Cons:**
- Need to find a way to handle secret passwords and tokens.
- "Inheritance" of settings can be hard to trace and maintain.

#### Environment Variables

**Pros:**
- Django config is separated from code.
- Environment parity – the same code for all environments.
- No inheritance in settings, cleaner and more consistent code.
- Theoretical grounding for using Django environment variables – 12 Factors.

**Cons:**
- Need to handle sharing default config between developers.

### Key Best Practices:

1. **Keep settings in environment variables:**
   - Enhances security by separating sensitive information from code.
   
2. **Write default values for production configuration (excluding secret keys and tokens):**
   - Ensures a fallback for crucial settings while avoiding exposure of sensitive information.

3. **Don’t hardcode sensitive settings, and don’t put them in VCS:**
   - Enhances security by preventing sensitive information from being exposed in version control.

4. **Split settings into groups: Django, third-party, project:**
   - Organizes settings for better readability and maintainability.

5. **Follow naming conventions for custom (project) settings:**
   - Improves code consistency and clarity by adhering to naming standards.

## WhiteNoise

A Python library that simplifies static file serving for Python web apps, enabling them to serve their own static files independently without external dependencies. Ideal for platforms like Heroku and OpenShift, it ensures deployment simplicity and high-traffic site performance when used with Content Delivery Networks (CDNs). Specifically designed for Django, WhiteNoise automates best practices, handling tasks such as compressed content serving and cache management.

### Setup

- Install WhiteNoise using pip:
  ```bash
  pip install whitenoise
  ```
- Add `whitenoise.middleware.WhiteNoiseMiddleware` to the `MIDDLEWARE` list in your `settings.py`, placing it above other middleware except Django's `SecurityMiddleware`:
  ```python
  MIDDLEWARE = [
      # ...
      "django.middleware.security.SecurityMiddleware",
      "whitenoise.middleware.WhiteNoiseMiddleware",
      # ...
  ]
  ```
- Optionally, for forever-cacheable files and compression support, add the following to your settings.py:
  ```python
  STATICFILES_STORAGE = "whitenoise.storage.CompressedManifestStaticFilesStorage"
  ```
- To enable WhiteNoise for other WSGI Apps, wrap your existing WSGI application in a WhiteNoise instance and specify the location of your static files. For example:
  ```python
  from whitenoise import WhiteNoise
  from my_project import MyWSGIApp

  application = MyWSGIApp()
  application = WhiteNoise(application, root="/path/to/static/files")
  application.add_files("/path/to/more/static/files", prefix="more-files/")
  ```

## CORS

Cross-Origin Resource Sharing (CORS) is a mechanism allowing restricted resources on a web page to be accessed from a different domain than the one serving the initial resource. It facilitates the embedding of cross-origin elements like images and scripts while defining a collaborative process between browsers and servers to ensure the safety of cross-origin requests. CORS strikes a balance by offering increased functionality compared to same-origin requests while maintaining security by preventing unrestricted cross-origin access.

### Setup

- Install the django-cors-headers package:
  ```bash
  pip install django-cors-headers

  ```
- Add corsheaders to your INSTALLED_APPS and MIDDLEWARE in your settings.py:
  ```python
  # settings.py

  INSTALLED_APPS = [
      # ...
      'corsheaders',
      # ...
  ]

  MIDDLEWARE = [
      # ...
      'corsheaders.middleware.CorsMiddleware',
      # ...
  ]

  ```
- Configure CORS settings in your settings.py:
  ```python
  # settings.py

  CORS_ALLOWED_ORIGINS = [
      "http://localhost:3000",  # Example: Allow requests from this origin
      "https://yourfrontenddomain.com",
  ]
  ```
  Adjust the CORS_ALLOWED_ORIGINS to include the domains you want to permit.

## Things I want to know more about