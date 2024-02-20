# Class 33

## JSON Web Tokens (JWTs)
JWTs are essential for secure information exchange, employing encoding and decoding to maintain data integrity and authenticity. They are commonly used for authentication and authorization processes.

### JWTs: Encoding and Decoding
- **Purpose:** Facilitates secure data exchange
- **Mechanism:** Utilizes encoding for data transfer
- **Algorithms:** Employed in decoding to ensure integrity
- **Authentication:** Provides a standardized method for verifying parties involved
- **Authorization:** Enables secure access to protected resources through decoded information

## JWT Authentication with Django REST Framework (DRF)
Integrating JWT Authentication with Django REST Framework (DRF) enhances API security through the use of tokens, acting as digital keys for accessing protected resources. This robust authentication mechanism involves key components, including authentication classes for validating user credentials and middleware ensuring a seamless integration of JWTs within the DRF ecosystem.

### Key Components
- **Tokens:** Act as digital keys providing access to protected resources
- **Authentication Classes:** Validate user credentials during the authentication process
- **Middleware:** Orchestrates the flow of requests and responses for seamless JWT integration
- **Enhanced Security:** Robust mechanism to fortify the overall security posture of API endpoints

## Django Deployment

While Django's built-in runserver is convenient for development due to its simplicity and ease of use, it comes with significant limitations that make it unsuitable for production environments. Some of these limitations include:

- **Single-threaded:** The built-in runserver is single-threaded, meaning it can only handle one request at a time. This severely impacts performance in a production setting with multiple concurrent requests.

- **Lack of robustness:** The built-in server lacks the robustness needed to handle the complexities and demands of a production environment. It may not effectively manage issues like load balancing, fault tolerance, and process management.

- **Security concerns:** The built-in server may not provide the level of security required for production applications. It lacks features such as process isolation and may expose potential vulnerabilities.

### Alternative Server Options for Django Deployment
- **Gunicorn:** Gunicorn is a reliable choice known for its ability to handle multiple concurrent requests through asynchronous workers. It provides better performance and scalability compared to the built-in server.

- **uWSGI:** uWSGI is a feature-rich server that excels in managing production workloads. It offers advanced features like process management, load balancing, and customization options, making it a popular choice for deploying Django applications in production.

- **Deployment Strategy:** Selecting the right server is crucial for a reliable and efficient hosting environment in real-world scenarios. Consideration of factors such as performance, scalability, and security is essential when choosing an alternative server for deploying Django applications.

## Things I want to know more about