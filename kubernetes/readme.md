# Kubernetes
## What is Kubernetes?
- Kubernetes is an open-source platform for automating the deployment, scaling, and management of containerized applications.

## Why should we use Kubernetes?
- Orchestration of containerized applications for efficient management at scale.
- Automated scaling and self-healing capabilities.
- Simplifies the deployment and management of microservices architectures.

## When should we use Kubernetes?
- When managing complex applications that consist of multiple containers.
- For scaling applications horizontally and efficiently handling high traffic.
- To ensure high availability and fault tolerance of applications.

## How can we use Kubernetes?
- Define application components and their dependencies in Kubernetes manifests (YAML files).
- Create deployments, services, and pods to run and manage applications.
- Use kubectl commands to interact with the Kubernetes cluster.

## Virtual Machines vs. Kubernetes Pods
- Virtual machines emulate physical hardware, while Kubernetes pods are groups of one or more containers sharing network and storage resources.

## Kubernetes Volumes
- Kubernetes volumes allow containers to persist data beyond the life cycle of individual pods, providing storage for applications.

## Kubernetes Logs
- Kubernetes logs capture the output and events from pods and containers, aiding in troubleshooting and monitoring application behavior.

## Development Environment with Kubernetes
- Kubernetes facilitates consistent development environments by defining application configurations in manifests and deploying them in clusters.

## Kubernetes Dashboard
### What is Kubernetes Dashboard?
- Kubernetes Dashboard is a web-based user interface for visualizing and managing Kubernetes clusters.

### Why should we use Kubernetes Dashboard?
- Provides a graphical interface for monitoring cluster resources and managing applications.
- Simplifies the monitoring and troubleshooting of Kubernetes deployments.

### When should we use Kubernetes Dashboard?
- When visualizing resource allocation, monitoring application health, and managing cluster resources.
- To simplify the management and deployment of applications through a user-friendly interface.

### How can we use Kubernetes Dashboard?
- Access the dashboard by running `kubectl proxy` and opening the dashboard URL in a web browser.
- View and manage cluster resources, monitor application health, and perform administrative tasks through the dashboard.

## Kubernetes Installation Guide
1. Download the latest version of kubectl and minikube for your operating system.
2. Install kubectl by following the official installation guide.
3. Install minikube by following the official installation guide.
4. Start a local Kubernetes cluster using minikube.
5. Verify the cluster is running with `kubectl get nodes`.
6. Congratulations! You have now set up a local Kubernetes cluster.


## Kubernetes Architecture

### Example of a Kubernetes deployment
```
---
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 3
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: martinmuraskovas/nginx-martin:latest
        ports:
        - containerPort: 80
```

### Architecture Overview:
- Replicas: 3 replicas of the nginx application.
- Selector: Used to select Pods based on labels. In my case, it selects Pods with the label app: nginx.
- Template: Defines the structure for the Pods created by the Deployment. It includes the Pod's labels and containers.
- Containers: Contains the configuration for the nginx container, including the image to use and the port to expose.

### Labels and Selectors:
- Labels: Key-value pairs attached to Kubernetes objects (like Pods). They are used to organize and select subsets of objects.
- Selectors: Define how you select objects based on their labels. They are used to link resources like Deployments with Pods.

### Diagram of Kubernetes Architecture
![alt text](k8architecture.png)

### Step by Step explanation of my nginx deployment
1. **apiVersion:** Specifies the version of the Kubernetes API being used.
2. **kind:** Defines the type of Kubernetes resource being created (Deployment in this case).
3. **metadata:** Contains information about the Deployment, such as its name.
4. **spec:**
   - **selector:** Defines how Pods are selected. In this case, it selects Pods with the label `app: nginx`.
   - **replicas:** Specifies the desired number of replicas (3 in your case).
   - **template:** Defines the Pod template.
     - **metadata:** Includes labels for the Pod.
     - **spec:** Specifies the Pod's specification.
       - **containers:** Contains configuration for the containers in the Pod.
         - **name:** Name of the container.
         - **image:** Specifies the Docker image to use.
         - **ports:** Specifies the ports to expose.
