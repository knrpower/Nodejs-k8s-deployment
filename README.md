# My Node.js and Kubernetes Project

This repository contains a simple Node.js application that is containerized using Docker and deployed on Kubernetes with specific network policies.

## Node.js Application

A simple Node.js application that listens on port 3000.

### Docker Setup

1. *Build the Docker Image*:
    sh
    docker build -t my-app-image:latest .
    

2. *Run the Docker Container*:
    sh
    docker run -p 3000:3000 my-app-image:latest

# Kubernetes Manifests

This directory contains the Kubernetes manifest files for deploying the Node.js application and the cache service, along with the network policy to restrict traffic.

## Files

- **my-app-deployment.yaml**: Deployment for the Node.js application.
- **cache-deployment.yaml**: Deployment for the cache service.
- **my-app-service.yaml**: Service to expose the Node.js application.
- **my-app-network-policy.yaml**: Network policy to restrict traffic.

## Applying the Manifests

1. **Apply the Deployments and Services**:
    sh
    kubectl apply -f my-app-deployment.yaml
    kubectl apply -f cache-deployment.yaml
    kubectl apply -f my-app-service.yaml
    kubectl apply -f my-app-network-policy.yaml
    

2. **Check the Status of the Deployments**:
    sh
    kubectl get deployments
    

3. **Check the Services**:
    sh
    kubectl get services
    

4. **Check the Network Policy**:
    sh
    kubectl get networkpolicy
    ```
