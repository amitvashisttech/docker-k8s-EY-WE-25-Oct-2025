# Kubernetes Resource Quotas Management Training & Development

This section covers the steps to manage Resource Quotas in Kubernetes, including creating namespaces, applying resource quotas, and managing deployments within those quotas.

## Commands Overview

### 1. Navigate to the Resource Quotas Directory

Change to the directory where the resource quotas and related YAML files are stored:

```bash
cd 11-Limits-and-Quotas/
```

### 2. Manage Resource Quota Configurations

#### a. Create a New Namespace

Create a new namespace called myspace:

```bash
kubectl apply -f 01-Namespace.yaml
```

### 3. Apply and Manage Deployments Without Quotas
#### a. Apply a Deployment Without Quotas

Apply a deployment in the myspace namespace without any resource quotas:

```bash
kubectl apply -f 02-Helloworld-deployment-without-limits.yaml
```

#### c. Verify Deployment

Check the pods in the myspace namespace:

```bash
kubectl get pods -n myspace
```
Delete the deployment without quotas:

```bash
kubectl delete -f 02-Helloworld-deployment-without-limits.yaml -n myspace
```
### 4. Apply and Manage Resource Request & Limits
#### a. Apply Default Resource Request & Limits 

Apply the defaults.yml file to set resource quotas in the myspace namespace:

```bash
kubectl apply -f 03-Default-Limits.yaml
kubectl get limitrange -n myspace
```
#### b. Apply a Deployment with Resource Quotas

Copy, modify, and apply a deployment file with resource quotas:

```bash
kubectl describe limitrange -n myspace
kubectl apply -f 02-Helloworld-deployment-without-limits.yaml
kubectl describe pod <<pod-name>> -n myspace
```
#### c. Verify the Deployment with Quotas

Check the status of the deployment and its associated pods:

```bash
kubectl get pods -n myspace
kubectl describe pods helloworld-deploymenti-with-quota-7478bb4645-7bjvx -n myspace
```
Delete the deployment with resource quotas:

```bash
kubectl delete -f 02-Helloworld-deployment-without-limits.yaml
```
### 5. Apply and Manage Specific Resource Quotas
#### a. Modify and Apply Resource Quotas


```bash
kubectl apply -f 05-Resource-Quota.yaml 
```
#### b. Verify Resource Quotas

Check the applied resource quotas in the myspace namespace:

```bash
kubectl get resourcequota -n myspace
```
### 6. Scale and Manage Deployments with Resource Quotas
#### a. Scale the Deployment

Scale the helloworld-deploymenti-with-quota deployment to 5 replicas:

```bash
kubectl scale --replicas=5 deploy helloworld-deploymenti-with-quota -n myspace
```
#### b. Verify Scaling

Check the status of the pods and the deployment:

```bash
kubectl get pods -n myspace
kubectl get deploy -n myspace
kubectl describe deploy helloworld-deploymenti-with-quota -n myspace
```

7. Cleanup and Resource Management
#### a. Delete Pods and Deployments

Delete specific pods and all pods in the myspace namespace:

```bash
kubectl delete pod helloworld-deploymenti-with-quota-569dc6fc8-ll6lf helloworld-deploymenti-with-quota-569dc6fc8-xzvv4 -n myspace
kubectl delete pod --all -n myspace --grace-period=0 --force
```

#### b. Final Verification

Check the final state of the pods and resource quotas:

```bash
kubectl get pods -n myspace
kubectl get resourcequota -n myspace
```
