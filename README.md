# Altschool K8s Deployment

## Overview

This project demonstrates the deployment of a sample application using **Kubernetes** (K8s) in a production-ready environment. The deployment process involves creating Kubernetes manifests for key resources such as deployments, services, and config maps to manage the application's lifecycle. The infrastructure is automated and maintained using best practices in DevOps, ensuring a scalable, reliable, and highly available setup.

## Table of Contents

- [Project Features](#project-features)
- [Prerequisites](#prerequisites)
- [Setup and Installation](#setup-and-installation)
- [Kubernetes Resources](#kubernetes-resources)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Features

- **Kubernetes Orchestration**: Manages application deployment, scaling, and operations.
- **Containerized Application**: The application is built and deployed using **Docker containers**.
- **Configuration Management**: Utilizes **ConfigMaps** and **Secrets** for environment configuration.
- **Service Discovery**: Exposes the application using **Kubernetes Services**.
- **Scalability**: Scalable deployment via **Kubernetes Horizontal Pod Autoscaler (HPA)**.

## Prerequisites

Before setting up the project, ensure you have the following installed:

- [Docker](https://www.docker.com/)
- [Kubernetes (kubectl)](https://kubernetes.io/docs/tasks/tools/)
- [Minikube](https://minikube.sigs.k8s.io/docs/) (or any Kubernetes cluster)
- [Helm](https://helm.sh/docs/intro/install/)
  
## Setup and Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Tijani891/altschool-K8s-Deployment.git
   cd altschool-K8s-Deployment
   ```

2. **Start Kubernetes Cluster**

   For Minikube:
   
   ```bash
   minikube start
   ```

3. **Deploy Application**

   Apply Kubernetes manifests to deploy the application:
   
   ```bash
   kubectl apply -f k8s/
   ```

4. **Verify Deployment**

   Check the status of the pods:
   
   ```bash
   kubectl get pods
   ```

5. **Expose the Application**

   To access the application, use Minikube’s service tunneling or expose the app with a LoadBalancer service:
   
   ```bash
   minikube service <service-name>
   ```

## Kubernetes Resources

This project makes use of the following Kubernetes resources:

- **Deployments**: Manages the desired state of application pods.
- **Services**: Exposes the application for internal or external traffic.
- **ConfigMaps**: Provides configuration data that can be consumed by the containers.
- **Secrets**: Stores sensitive information like database credentials.
- **Horizontal Pod Autoscaler (HPA)**: Automatically scales the application pods based on resource usage.

## Usage

- **Testing**: You can test the application's functionality by accessing the service URL exposed via Minikube or Kubernetes service. 
- **Scaling**: To manually scale the application:
  
  ```bash
  kubectl scale deployment <deployment-name> --replicas=3
  ```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request or open an Issue to discuss improvements or report bugs.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
