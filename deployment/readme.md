# Deployment
A kubernetecs deployment is a higher-level resource in kubernetes that provides declarative updates for pods and ReplicaSets. It manages the lifecycle of application, ensuring that a specified number of Pod replicas are running and handling updates and rollback in a controller manner. 

### ReplicaSets
A ReplicaSet in Kubernetes is a controller that ensures a specified number of identical Pod replicas are running at all times. It is a key componet for maintaining application availability and enabling self-healing capabilities within a kubernetes cluster. 

## Kubernetes Deployment entails:
- Define the desire state of application with the deployment manifest. (e.g. how many Pods should run, which container image to user how updates should be applied)

- A Deployment creates and manage ReplicaSets, which in turn manage the creating and scaling of individual pods. This abstraction simplifies the management of multiple Pod replicas. 

- Deployment facilitate rolling updates, allowing to update application with new versions without downtime. This involves gradually replacing old Pods with new ones, ensuring continuous availability. 

- If an update introduces issue, Deployments enable easy rollback to a previous stable version of an application

- If Pod or the node it's running of fails, the Deployment controller automatically replaces it, providing resilience and high availbility. 

- Scaling application up and down by adjusting the number of replicas. 

## Imperative way to create deployment
```
kubectl create deployment "Name_OF_Deployment" --image="Image name"
```