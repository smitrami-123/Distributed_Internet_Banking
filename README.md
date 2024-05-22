**Internet Banking Microservices with Spring Cloud Config**

This repository contains a set of microservices built using Spring Boot and Spring Cloud Config for managing centralized configurations. The microservices architecture includes services for user management, utility payments, fund transfers, and more, all integrated with a central configuration server.

### Features

- **Centralized Configurations**: Utilizes Spring Cloud Config Server to manage application configurations centrally.
- **Microservices Architecture**: Implements a distributed architecture with multiple independent microservices.
- **RESTful APIs**: Provides RESTful APIs for various functionalities such as user registration, fund transfers, and utility payments.
- **Secure Configuration Management**: Supports both public and private repositories for storing application configurations securely.

### Services

1. **User Service**: Manages user registration and authentication.
2. **Fund Transfer Service**: Facilitates fund transfer between user accounts.
3. **Utility Payment Service**: Handles utility payments such as electricity, water, and gas bills.
4. **Banking Core Service**: Manages accounts, users, transaction details, and banking transactions.
5. **Notification Service**: Consumes messages from RabbitMQ and sends necessary notifications to end users.

### Getting Started

1. **Clone the Repository**: Clone this repository to your local machine using `git clone`.

2. **Setup Configuration Server**:
   - Navigate to the `internet-banking-config-server` directory.
   - Configure the Spring Cloud Config Server by providing the Git repository URL in `application.yml`.
   - Start the configuration server by running the Spring Boot application.

3. **Configure Microservices**:
   - Navigate to each microservice directory (e.g., `internet-banking-user-service`).
   - Update the `bootstrap.yml` or `bootstrap.properties` file to point to the configuration server.
   - Remove local configurations from `application.yml` or `application.properties`.
   - Start each microservice by running the Spring Boot application.

4. **Accessing Configurations**:
   - Once the configuration server and microservices are running, access the configurations using the following endpoints:
     - Configuration Server: `http://localhost:8090/{microservice-name}/{profile}`
     - Example: `http://localhost:8090/internet-banking-user-service/default`

5. **Testing APIs**:
   - Use tools like Postman to test the RESTful APIs exposed by the microservices.
   - Refer to the API documentation or source code for available endpoints and request/response formats.

### Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/NewFeature`).
3. Commit your changes (`git commit -am 'Add NewFeature'`).
4. Push to the branch (`git push origin feature/NewFeature`).
5. Create a new Pull Request.



### Acknowledgments

Special thanks to the contributors and the community for their valuable feedback and support.

---
**Internet Banking Microservices with Spring Cloud Config** - Developed by [Smit Rami](https://github.com/smitrami-123)
