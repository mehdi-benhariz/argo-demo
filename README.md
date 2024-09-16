# Guestbook UI Demo

This is a simple demo project for testing Argo CD. It deploys a basic web application showing a guestbook UI.

## Deploying with Argo CD

1. Create a new application in Argo CD.
2. Set the repository URL to this GitHub repository.
3. Set the path to `k8s` (ensure your Kubernetes manifests are located here).
4. Set the destination to your target Kubernetes cluster and namespace.

## Kubernetes Deployment and Service

The deployment uses the `gcr.io/heptio-images/ks-guestbook-demo:0.2` image and exposes it on port 80. The service `guestbook-ui` is also set up to route traffic to port 80 of the deployed containers.

## Accessing the application

After deployment, access the application by port-forwarding the service:

Then, open a web browser and navigate to `http://localhost:8080`.