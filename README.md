# Distributed IoT Application Platform

The Distributed IoT Application Platform makes it easy for users to set up and manage their IoT projects. It connects effortlessly with different sensors and uses the oneM2M platform to collect data. Designed to be user-friendly, this platform offers flexible settings, strong security, and smart resource use.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Functional Requirements](#functional-requirements)
4. [Non-Functional Requirements](#non-functional-requirements)
5. [External Interface Requirements](#external-interface-requirements)
6. [Folder Structure](#folder-structure)
7. [Microservices Details](#microservices-details)
8. [Demo Video](#demo-video)
9. [Communication Diagram](#communication-diagram)
10. [Architecture Diagram](#architecture-diagram)
11. [Future Scope](#future-scope)
12. [Getting Started](#getting-started)
13. [License](#license)
14. [Contributing](#contributing)

## Introduction

The Distributed IoT Application Platform is a project that aims to design and develop a platform where users can run and host their IoT-based applications. This platform provides the capability to interact with various sensors independent of their type, making it flexible and adaptable to different IoT scenarios. The project leverages the oneM2M platform for data gathering, ensuring compatibility with various protocols.

The platform is designed to dynamically understand the application requirements through configuration files. It intelligently selects the most efficient workflows for building and deploying IoT applications, optimizing performance and resource utilization. This dynamic approach allows users to easily adapt and customize the platform based on their specific needs.

The primary purpose of the Distributed IoT Application Platform is to enable organizations to deploy and manage large-scale IoT solutions securely and in a scalable manner. It provides end-to-end functionality, including device and application connectivity, device and data management, data analysis, and security features. The platform empowers users to gain real-time insights, optimize processes, and automate tasks, leading to improved operational efficiency and enhanced decision-making.

## Features

- Real-time data analysis from various IoT sensors.
- Effective anomaly detection mechanism.
- RESTful APIs for seamless data access.
- Standardized machine-to-machine communication using OneM2M.
- Integration capabilities with AWS/Azure for resource management.

## Functional Requirements

### **Application**

- API-driven **Sensor Interaction** with integrated sensor manager.
- Independent **App Development** leveraging platform APIs.
- Unique ID-based **Sensor Identification**.
- Efficient **Data Binding** from sensors to applications.

### **Communication**

- Scalable **Message Handling** with reliable delivery.
- Robust **Access Management** using authentication/authorization.

### **Server & Deployment**

- Automated server initiation on new app deployment.
- **Monitoring** capabilities with strong **Security** (API keys, LDAP, JWT).

### **Load Balancing**

- Methods and tools for even microservice distribution.

### **Module Interactions**

- Coordinated modules via communication, data sharing, and control mechanisms.

### **Packaging & Configuration**

- Bundled packaging of essential files.
- Flexible **Configurations** in XML or JSON.

### **Actors**

- Devices process and act based on platform data.

## Non-Functional Requirements

### **Fault Tolerance**

- **Platform:** Achieve redundancy through multiple instances to handle potential failures.
- **Application:** Seamless error handling to ensure uninterrupted user experience.

### **Scalability**

- **Platform & Application:**
  - Modular architecture.
  - Horizontal scaling.
  - Asynchronous processing.
  - Utilize Kafka for distributed architecture, replication, and high throughput.

### **Accessibility of Data**

- **Application:** Use REST APIs for data access.
- **Sensors:** Integration of OneM2M with ThingsBoard for standardized data management and MQTT for receiving data.

### **Application Specifications**

- **Reliability:** Consistent performance with minimal failures.
- **Performance:** Optimal speed, throughput, and response time.
- **Usability:** Intuitive design that caters to user needs.

### **Interaction Interfaces**

- Terminal-based UI for platform interaction.

### **Security**

- Password-based authentication.
- LDAP for authorization.

### **Monitoring**

- Utilize ThingsBoard.io server-side APIs for secure monitoring and control of IoT entities.

### **Persistence**

- Approaches under consideration:
  - File-based persistence.
  - Relational and non-relational databases.

## External Interface Requirements

- OAuth support for authentication.
- APIs for managing bare metal resources from AWS/Azure.

## Folder Structure

The project is organized as follows:

- **`project-root-directory/`**
  - **`client/`**
    - `src/`: Client-side source files for the UI and interactions.
  - **`server/`**
    - `ApplicationManager/`: Manages the lifecycle of applications and services.
    - `Bootstrap/`: Initial setup and configurations for the platform.
    - `Logger/`: Logging utilities for tracking system activities.
    - `analytics/`: Provides data analytics and insights.
    - `api-manager/`: Manages the API endpoints and routing.
    - `api/`: API endpoints and related functionality.
    - `docs/`: Documentation and guides for the platform.
    - `extras/`: Additional utilities and helper scripts.
    - `load-balancer/`: Distributes incoming traffic across services for optimal performance.
    - `monitoring-service/`: Monitors the health and performance of services.
    - `node-manager/`: Handles node-related operations and lifecycle.
    - `notification-manager/`: Manages notifications and alerting.
    - `schema/`: Database schema and related utilities.
    - `sensor-manager/`: Manages sensor integrations, data collection, and interactions.

## Microservices

### 1. Monitoring Service

- **Description:** Monitors the health and performance of services. Uses server-side APIs provided by `ThingsBoard.io` to oversee and control IoT entities securely.

### 2. Load Balancing Service

- **Description:** Distributes incoming traffic across the platform's services, ensuring optimal performance and efficient resource utilization.

### 3. Node/VM Manager and Deployment Manager

- **Description:** Manages node-related operations and their lifecycle. Oversees deployment of services and applications on nodes or VMs.

### 4. API Manager

- **Description:** Manages the API endpoints and routing, ensuring a streamlined interface for both internal and external communications.

### 5. Communication Manager

- **Description:** Responsible for managing inter-service communication, maintaining data integrity and reliability.

### 6. Deployment Manager and Bootstrap Service

- **Description:** Handles initial platform setups, configurations, and the proper deployment of services.

### 7. Sensor Manager

- **Description:** Manages sensor integrations and interactions. Uses `OneM2M` for standardizing M2M communications and integrates with `ThingsBoard` via MQTT for data collection and visualization.

## Communication Diagram

The communication diagram provides a clear representation of the information flow within the Distributed IoT Application Platform. It emphasizes the interactions between various components and services to ensure smooth data transmission and processing.

![Communication Diagram](https://github.com/bhanujggandhi/iot-platform-project/blob/main/artifacts/Communication%20Model.jpg)

## Architecture Diagram

To understand the structural layout and interdependencies of the platform components, refer to the architecture diagram. It gives a comprehensive view of the system design, making it easier for users and developers to grasp the platform's intricacies.

![Architecture Diagram](https://github.com/bhanujggandhi/iot-platform-project/blob/main/artifacts/Architecture%20Diagram.jpg)

## Demo Video

Get a firsthand experience of the Distributed IoT Application Platform in action. Click the video below to watch the demo:

<https://github.com/bhanujggandhi/iot-platform-project/assets/41260948/70dd75a6-11cc-42a9-814d-ee760bd8a3ef>

## Future Scope

- **Broader Integration**: Plan to connect with even more types of IoT devices for versatility.
- **Smarter Analysis**: Upgrade data processing tools for clearer insights from the gathered data.
- **Safety First**: Boost security to keep both users and their devices safe.
- **Ease of Use**: Streamline user interfaces and workflows for a more user-friendly experience.
- **Growing with Demand**: Prepare the platform to effortlessly handle increased device connections and data volume.

## Getting Started

Welcome to our IoT platform, designed to manage, process, and visualize data from various connected devices with a keen focus on fault tolerance, scalability, and security. Here's how you can get started:

### 1. **Setup Instructions**

- **Platform Installation:**
  - Clone the project repository.
  - Navigate to the project directory.

- **Application Deployment:**
  - Ensure your application meets platform compatibility requirements (OS, programming language, dependencies).
  - Deploy your application using the provided deployment script or tools.
  - More details are availableat docs on deployment. You can refer that.
  
### 2. **Dependencies**

- **Kafka:** Our platform relies heavily on Kafka for distributed architecture, replication, and high throughput.
  - [Download Kafka](https://kafka.apache.org/downloads)
  - Follow the installation guide specific to your operating system.

- **ThingsBoard:** Integration of sensors and visualization relies on ThingsBoard.
  - [Download ThingsBoard](https://thingsboard.io/download/)
  - Follow the setup instructions.

- **OneM2M:** Standard for Machine-to-Machine communications.
  - Ensure your devices or sensors support OneM2M.
  - Configure them to send data using MQTT to the platform.

### 3. **Configuration**

- **Application Configuration Files:**
  - Navigate to the configuration directories of each microservices(e.g., `./config/`).
  - Adjust default settings in XML or JSON format files as per your application needs.

- **Platform Security:**
  - Set up password-based authentication or LDAP as needed.
  - Ensure API keys for platform APIs are safely stored and used.

- **Sensor Registration:**
  - Register your sensors on the IoT platform.
  - Make note of unique sensor IDs and metadata for interaction with applications.

By following the above steps, you should have the platform up and running, ready to process and visualize data from your IoT devices. For further assistance, refer to our detailed documentation or reach out to our support team.

## contributing

Feel free to explore the source code repository, watch the demo video, and refer to the communication and architecture diagrams to get a better understanding of the Distributed IoT Application Platform.

## License

MIT License.
