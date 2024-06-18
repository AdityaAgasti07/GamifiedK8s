# Gamified-K8s
## KubeDoom is a unique project that combines the Kubernetes with the classic first-person shooter video game Doom. It provides a gamified user interface for managing Kubernetes clusters, making the process more engaging and enjoyable
# Kubedoom
Kubedoom is a project that demonstrates the deployment and execution of the classic first-person shooter game Doom on a Kubernetes cluster. It serves as an educational and entertaining example of running applications on Kubernetes.

## Description
This project showcases the steps involved in setting up a Kubernetes cluster, building a Docker image for Doom, and deploying the game as a pod on the cluster. It provides a hands-on experience in working with Kubernetes concepts such as pods, deployments, services, and more.

## Key Concepts
### Kubernetes
Kubernetes is an open-source container orchestration platform used for automating the deployment, scaling, and management of containerized applications. It provides a declarative approach to managing applications, ensuring high availability, scalability, and efficient resource utilization.

### Pods
In Kubernetes, a pod is the smallest deployable unit of computing that can be created and managed. It is a group of one or more containers sharing storage and network resources, and specifications for running the containers.

### Deployments
A Deployment is a Kubernetes resource that provides declarative updates for Pods and ReplicaSets. It ensures that the desired number of replicas of a Pod are running at any given time. Deployments handle rolling updates, rollbacks, and scaling.

### Services
A Service is an abstraction layer that defines a logical set of Pods and a policy for accessing them. It acts as a load balancer and provides a stable IP address and DNS name for accessing the Pods.

## Prerequisites
- Kubernetes cluster (local or cloud-based)
- Docker
- Git

## Installation

1. Clone the repository:
``` bash
git clone https://github.com/your-repo/kubedoom.git
```
3. Navigate to the project directory:
```bash
cd kubedoom
```
5. Build the Doom Docker image:
```bash
docker build -t doom .
```
7. Deploy Doom to the Kubernetes cluster:
```bash
kubectl apply -f doom-deployment.yaml
```
9. Expose the Doom pod as a service:
```bash
kubectl apply -f doom-service.yaml
```
11. Access the Doom game by connecting to the exposed service.

## Usage
Once the Doom pod is running and the service is exposed, you can connect to the game using a VNC client or a web-based VNC viewer. The connection details (IP address, port, and password) will be displayed in the logs or can be obtained by running:
```bash
kubectl get svc doom
```
After connecting, you can interact with the Doom game using the keyboard and mouse controls.
## Cleanup
To remove the Doom deployment and service from the cluster, run:
```bash
kubectl delete deployment doom
kubectl delete service doom
```
## Additional Information

- **Persistent Storage**: Depending on your requirements, you may want to configure persistent storage for saving game progress or storing game data.

- **Scaling**: Kubernetes allows you to scale the number of Doom Pod replicas up or down based on demand.

- **Monitoring and Logging**: Kubernetes provides built-in monitoring and logging capabilities, which can be useful for tracking the performance and behavior of your Doom deployment.

- **Networking**: Kubernetes offers advanced networking features, such as load balancing, ingress routing, and network policies, which can be utilized for managing traffic to your Doom game.

## Contributing

Contributions are welcome! If you have any suggestions, improvements, or bug fixes, please open an issue or submit a pull request.

