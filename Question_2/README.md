
# MERN Application Kubernetes Deployment

## Overview
This document contains all commands used to deploy a MERN stack application on Kubernetes.

## Deployment Commands

### 1. Create Namespace
```bash
kubectl apply -f namespace.yaml
```
Creates the `i211197-mern-app` namespace for isolating application resources.

### 2. Create MongoDB PersistentVolumeClaim
```bash
kubectl apply -f mongodb-pvc.yaml
```
Provisions 5Gi storage for MongoDB data persistence.

### 3. Deploy MongoDB
```bash
kubectl apply -f mongodb-deployment.yaml
```
Deploys MongoDB instance with ClusterIP service on port 27017.

### 4. Deploy Backend API
```bash
kubectl apply -f backend-deployment.yaml
```
Deploys 2 replicas of backend service on NodePort 30300 (port 6868).

### 5. Deploy Frontend UI
```bash
kubectl apply -f frontend-deployment.yaml
```
Deploys 2 replicas of frontend service on NodePort 30173 (port 8888).

### 6. Deploy All Resources
```bash
kubectl apply -f .
```
Applies all YAML files in the current directory.

### 7. Verify Deployments
```bash
kubectl get all -n i211197-mern-app
```
Lists all pods, services, and deployments in the namespace.

### 8. Check Pod Logs
```bash
kubectl logs <pod-name> -n i211197-mern-app
```
Displays logs from a specific pod for debugging.

### 9. Delete Deployment
```bash
kubectl delete namespace i211197-mern-app
```
Removes the entire namespace and all associated resources.
