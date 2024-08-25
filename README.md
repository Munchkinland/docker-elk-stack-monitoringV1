# Docker ELK Stack Monitoring

![f2f2ca74-c2b6-44cd-911d-24dd66be8a9a](https://github.com/user-attachments/assets/53fdbd04-597c-4b44-bce7-5245316e1d33)

## Overview

This project sets up a comprehensive monitoring solution using Docker, the Elastic Stack (ELK Stack), and Beats. It includes services for Elasticsearch, Kibana, Heartbeat, Metricbeat, and Portainer, along with a sample Python application for testing.

## Features

- **Elasticsearch**: Stores and indexes monitoring data.
- **Kibana**: Provides a web interface for visualizing data and dashboards.
- **Heartbeat**: Monitors the availability and response time of services.
- **Metricbeat**: Collects system and Docker metrics and sends them to Elasticsearch.
- **Portainer**: A web-based Docker management tool for easy container management.
- **ping_app**: A sample Python application for testing and demonstration.

## Services

- **Elasticsearch**: Provides full-text search and analytics capabilities.
- **Kibana**: Offers data visualization and dashboard functionalities.
- **Heartbeat**: Checks the availability of HTTP, TCP, and ICMP endpoints.
- **Metricbeat**: Collects metrics from Docker containers and the host system.
- **Portainer**: A web-based Docker management tool to view and manage your Docker containers.
- **ping_app**: A simple Python application that listens on port 8080 and can be used to test monitoring setups.

## Getting Started

### Prerequisites

- Docker
- Docker Compose

### Installation

### 1. Clone the repository:

git clone https://github.com/Munchkinland/docker-elk-stack-monitoring.git 
cd docker-elk-stack-monitoring
   
### 2. Build and start the services:

docker-compose up -d

### 3. Access the services:

Kibana: http://localhost:5601
Portainer: http://localhost:9000
Ping App: http://localhost:8080

### 4. Configuration
Heartbeat: Monitors HTTP, TCP, and ICMP endpoints. Configure heartbeat.yml for custom monitors.
Metricbeat: Collects system and Docker metrics. Configure metricbeat.yml to enable or disable specific modules.

### 5. Example Queries
List all containers:

GET /_cat/indices?v
Search for logs related to a specific application:

GET /metricbeat-*/_search
{
  "query": {
    "match": {
      "process.name": "calculator"
    }
  }
}

# Using Portainer
Portainer provides a graphical interface to manage your Docker containers. You can use it to start, stop, and monitor the status of your containers.

## Using ping_app
ping_app is a simple Python application that you can use to test your monitoring setup. It listens on port 8080. You can make HTTP requests to this application to check if it is being monitored correctly.

## Contributing
Feel free to open issues or submit pull requests if you have suggestions or improvements. Please follow the contributing guidelines.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# Contact
For any questions or feedback, please feel free to contact me on https://www.linkedin.com/in/rub%C3%A9n-carrasco-143145135/
