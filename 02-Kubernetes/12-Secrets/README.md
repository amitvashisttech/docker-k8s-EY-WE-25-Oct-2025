# Kubernetes Secrets - Hands-On Lab

This directory contains example commands and manifests for working with Kubernetes Secrets using `kubectl` and `oc`.

---

## 1. Create a Working Directory

```bash
cd 12-Secrets/
```

## 2. View Existing Secrets
```
kubectl get secrets
```

## 3. Explore Secret Creation Commands
```
kubectl create secret generic test-secrets --help     # Correct help command

```

## 4. Create Secret from Literal Values (Dry Run)
```bash
kubectl create secret generic test-secrets \
  --from-literal=Demo=EY \
  --from-literal=Location=Noida \
  --dry-run=client -o yaml
```

## 5. Create Secret for Real
```
kubectl create secret generic test-secrets \
  --from-literal=Demo=EY \
  --from-literal=Location=Noida
```

## 6. Verify Secret
```
kubectl get secrets
```

## 7. Create Secret Using YAML
```
cat 1-hello-secrets.yaml
kubectl apply -f 1-hello-secrets.yaml
```
```
kubectl get secrets
kubectl describe secrets my-db-secrets
kubectl edit secrets my-db-secrets
```

## 8. Create Deployment That Mounts Secret as Volume
```
cat 2-helloworld-secret-vol.yaml
kubectl apply -f 2-helloworld-secret-vol.yaml
```

## 9. Access Secret Inside Pod
```
kubectl exec -it <<pod-name>> -- ls /etc/
kubectl exec -it <<pod-name>> -- ls /etc/creds/
kubectl exec -it <<pod-name>> -- cat /etc/creds/username
```
 
