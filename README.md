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
cd postgres
kubectl apply -f postgres-config.yaml
kubectl apply -f postgres-secret.yaml
kubectl apply -f postgres-storage.yaml
kubectl apply -f postgres-deployment.yaml
kubectl apply -f postgres-service.yaml
```

#### Connexion at postgres 


```bash
kubectl exec --stdin --tty <Pod_Name> -- psql -U postgresadmin -d postgresdb -W
```
