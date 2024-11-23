# School Management Configuration

This repository contains the centralized **Spring Cloud Config** files for the **School Management Application**. These configuration files provide externalized settings for the microservices within the application, allowing centralized management of environment-specific properties and ensuring dynamic updates without the need to redeploy services.

---

## Application Overview

The **School Management Application** is a microservices-based system with the following key components:

1. **Teacher Service**
2. **Student Service**
3. **Exam Service**
4. **API Gateway**
5. **Eureka Discovery Server**
6. **Config Service**

This configuration repository is integrated with **Spring Cloud Config Server**, which fetches properties from this repository and distributes them to the microservices.

---


## Configuration File Example

### 1. **application.yml**
Contains common configurations shared across all services. Example:

```yaml
spring:
  application:
    name: school-management
  cloud:
    config:
      server:
        git:
          uri: https://github.com/rayennebr/school-management-configuration
          default-label: main
