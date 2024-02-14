# Class 29

## Custom User Model

**Benefits of Django Custom User Model:**
- **Flexibility**: Allows you to define custom fields tailored to your application's requirements.
- **Scalability**: Provides a scalable solution for managing user data as your application grows.
- **Security**: Enables you to implement custom authentication methods and enhance security measures.
- **Simplicity**: Simplifies user management by centralizing user-related logic within your application.
- **Compatibility**: Ensures compatibility with third-party packages and extensions that rely on a custom user model.

**Differences from Default Django User Model:**
- **Field Customization**: You can add additional fields such as profile information, contact details, or preferences.
- **Authentication**: Allows you to implement custom authentication methods beyond the default username/email and password combination.
- **User Identification**: Provides flexibility in how users are identified, such as using email addresses or unique usernames.
- **Integration**: Facilitates integration with existing databases or user systems by defining the user model according to your data structure.
- **Extensibility**: Allows for easy extension with additional functionality or behavior specific to your application's needs.

### Creating Custom User Model

- **Setup:**
  - Create a new Django project from the command line.
  - Navigate into a dedicated directory called 'accounts' for code.
  - Install Django, make a new project, make a new app called 'accounts,' and start the local web server.

- **AbstractUser vs AbstractBaseUser:**
  - Two ways to create a custom user model: AbstractUser and AbstractBaseUser.
  - AbstractUser is recommended for its default configuration, while AbstractBaseUser requires more work.

- **Custom User Model:**
  - Update `settings.py` to include the 'accounts' app and configure `AUTH_USER_MODEL` to use the new custom user model.
  - Create a new model named `CustomUser` in `accounts/models.py`.
  - Define additional fields within the `CustomUser` model.

- **Form Creation:**
  - Create new versions of UserCreationForm and UserChangeForm in a new file `accounts/forms.py`.
  - Subclass the existing forms and use the `CustomUser` model.

- **Admin Configuration:**
  - Update `accounts/admin.py` to use the new forms and model for admin customization.

- **Database Migration:**
  - Run `makemigrations` and `migrate` to create a new database using the custom user model.

- **Superuser Creation:**
  - Create a superuser using `createsuperuser` command for admin access.

- **Templates/Views/URLs:**
  - Configure project-level templates directory in `settings.py`.
  - Set redirect links for login and logout in `settings.py`.
  - Create templates for home, login, signup, and base.

- **URL Configuration:**
  - Update project-level and app-level `urls.py` files for routing.

- **Views Configuration:**
  - Create `accounts/views.py` file containing a SignUpView class with form configuration.

- **Testing:**
  - Start the server and navigate to the homepage.
  - Test login, logout, and signup functionalities.
  - Verify superuser access in the admin panel.

- **Conclusion:**
  - Custom user model configured, allowing easy addition of additional fields.
  - Consider DjangoX for a starter framework with more features.
  - Explore 'Django for Beginners' book for an in-depth Django project example.

## DjangoX

DjangoX is an open-source Django starter framework that complements and extends the functionality of Django by providing additional features and a pre-configured project structure. It aims to streamline the development process and includes enhancements beyond the default Django setup.

**Key Features of DjangoX:**
- **Custom User Model:** DjangoX includes a custom user model with email/password authentication by default, offering improved security practices.

- **Social Authentication:** It supports social authentication out of the box, allowing users to sign in using social media accounts.

- **Additional Django Packages:** DjangoX comes with pre-installed Django packages for common functionalities, reducing the need for manual configuration. This includes packages for handling forms, emails, and more.

- **Bootstrap Integration:** The framework integrates Bootstrap for frontend styling, providing a clean and responsive design from the start.

- **Django Rest Framework:** DjangoX includes Django Rest Framework for building APIs, extending the project's capabilities to handle RESTful services.

**Example Use Case:**
Suppose you are starting a new web application that requires user authentication, social login capabilities, and a clean, responsive design. Instead of configuring these features manually in a vanilla Django project, you can use DjangoX to jumpstart your development process.

By incorporating DjangoX into your project, you can quickly leverage the custom user model, social authentication, and Bootstrap styling without spending time on initial setup. This allows you to focus more on implementing your application's unique features and functionality.

## Things I want to know more about
