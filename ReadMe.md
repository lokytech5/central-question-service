## 📸 Central Service for Question-Service

### Overview
This central service is designed to orchestrate and run a subsection of Personalized Learning Management System, which includes the Question Service, User Service, and Service Registry. It simplifies the process of deploying and managing these interdependent services by utilizing Docker and Docker Compose.


## Architecture
The system comprises several services, each running in its own Docker container:

- User Service: Manages user-related functionalities.
- Question Service: Handles user-generated questions and AI-driven answers.
- Service Registry: Eureka server for service discovery.
- User Database and Question Database: Separate MySQL instances for user and question data.
- Zipkin Server: For distributed tracing.


## Prerequisites
- Docker and Docker Compose installed on your system.
- Basic understanding of Docker and containerization concepts.

## Configuration
Before running the services, ensure you have set the necessary environment variables in a .env file or in your environment. These include:

- `MYSQL_ROOT_PASSWORD`
- `MYSQL_DATABASE_USERS_SERVICE`
- `MYSQL_DATABASE_QUESTION_SERVICE`
- `MYSQL_USER`
- `MYSQL_PASSWORD`
- `DB_USERNAME`
- `DB_PASSWORD`
- `EUREKA_CLIENT_SERVICEURL_DEFAULTZONE`
- `MANAGEMENT_ZIPKIN_TRACING_ENDPOINT`


## Running the Services
1. Clone this Repository:
   - `git clone [URL-of-this-central-service-repository]`

2. Navigate to the Repository Directory:
   - `cd [repository-directory-name]`
  
3. Start the Services using Docker Compose:
   - `docker-compose up`

This will pull the necessary Docker images and start the containers as defined in the `docker-compose.yml` file.

4. Verifying the Setup:

- The User Service will be accessible on port `8000`.
- The Question Service will be accessible on port `8200`.
- The Eureka Service Registry will be accessible on port `8761`.
- Zipkin Server for tracing will be available on port `9411`.

## Using the Services
Once all services are up and running, you can interact with each service through their respective endpoints. For example, you can access the Question Service's endpoints to manage and respond to user-generated questions.

## Troubleshooting
If you encounter any issues while setting up or running the services, please check the following:

- Ensure all environment variables are correctly set.
- Verify Docker and Docker Compose are correctly installed and running.
- Check the container logs for any service-specific errors.
  
## 📜 License
This project is licensed under the MIT License.

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! See our contributing guide for more details.