# infrastructure

### Prérequis
```bash
minikube start
```
#### Apply postgres 
Ce fichier définit le mot de passe qui sera utilisé lors de la connexion au serveur  Postgres.
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