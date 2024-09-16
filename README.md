# Solar System Demo

This is a simple demo project for testing Argo CD. It deploys a basic web application showing a visualization of the solar system.

## Building the Docker image

```
docker build -t your-docker-username/solar-system-demo:v1 .
docker push your-docker-username/solar-system-demo:v1
```
## Deploying with Argo CD

1. Create a new application in Argo CD
2. Set the repository URL to this GitHub repository
3. Set the path to `k8s`
4. Set the destination to your target Kubernetes cluster and namespace

## Accessing the application

After deployment, you can access the application by port-forwarding the service:

```
kubectl port-forward svc/solar-system-demo 8080:80
```

Then open a web browser and go to `http://localhost:8080`