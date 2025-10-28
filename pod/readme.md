# Pods
In Kubernetes, a Pod is the smallest and most fundamental deployable unit you can create and manage. It represents a single instance of a running process in your cluster. 

## Diferent ways of creating kubernetes objects
- Imperative way (Throught command or API calls)
- Declarative Way (By creating manifest files (YAML files))

![alt text](image.png)

- Create a pod using the imperative command and use nginx as the image

```bash 
kubectl run nginx(Name of the pod) nginx
```

Command to apply ymal file 

```
kubectl apply -f "File path" --namespace=(Optional)
```