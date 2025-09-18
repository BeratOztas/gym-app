# Gym-App

Gym-App is a microservice-based application for a gym's Customer Relationship Management (CRM) system. It is designed to demonstrate a monorepo structure using Maven for dependency management and Docker Compose for service orchestration.

## -- Project Structure
The project follows a monorepo structure, with all microservices located in a single directory.

- **discovery-service**: Eureka-based service discovery for microservices.
- **gym-crm**: The core CRM application logic.
- **trainer-hours-service**: A dedicated service for managing and processing trainer work hours.
- **training-commons**: A shared library module containing common classes and utilities.
- **docker-compose.yml**: The main orchestration file to run all services together.
- **pom.xml**: The parent Maven project file managing all sub-modules.

## -- Getting Started
Follow these steps to set up and run the project locally.

### -- Prerequisites
- **Java 17 or higher**: The project is built with Java 17.
- **Maven**: Used for building the project.
- **Docker & Docker Compose**: Required to run the services.

### -- Build the Project
Navigate to the main `gym-app` directory and build all microservice JAR files:

```bash
mvn clean install
-- Start the Services
Use Docker Compose to build and start all the services:

```bash 
docker-compose up --build
-- Local Development (IDE)
If you prefer to work on a specific microservice in your IDE (Eclipse, VS Code, etc.), import the parent pom.xml file. Your IDE will automatically detect all modules as separate projects.

-- Accessing Services
Once the services are running, you can access them at the following URLs:

Discovery Service (Eureka): http://localhost:8761

Gym CRM Service: http://localhost:8080

Trainer Hours Service: http://localhost:8081

-- License
This project is open-source and available under the MIT License.