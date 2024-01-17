# infrastructure

### Prérequis
```bash
minikube start
```

#### Launch Deployment and Service of our both services
```bash
kubectl apply -f microservices.yaml
```

#### Launch Ingress 
```bash
kubectl apply -f infrastructure.yaml
```

#### Launch postgres 

```bash 
kubectl apply -f postges-secret.yaml
kubectl apply -f postges-storage.yaml
kubectl apply -f postges-deployment.yaml
kubectl apply -f postges-service.yaml
```

#### Connexion at postgres 


```bash
kubectl exec --stdin --tty <Pod_Name> -- psql -U postgresadmin -d postgresdb -W
```
