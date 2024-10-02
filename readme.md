# Comandos kubernetes

kubectl get nodes
kubectl get services
kubectl get deployments
kubectl get pods
kubectl get configmap
kubectl get secret

kubectl port-forward svc/postgres-service 5432:5432

kubectl apply -f demo/postgresql/

kubectl delete -f demo/postgresql/

PAra ver los logs
kubectl logs nombre-del-pod

Permite entrar dentro de un contenedor dentro de un pod.

kubectl exec -it nginx-deployment-7c79c4bf97-kkz4n -- /bin/sh

kubectl delete po nginx-deployment-7c79c4bf97-2ktd7 nginx-deployment-7c79c4bf97-7klxx

Ejemplo de conexión a la base de datos

```sh
PGPASSWD=mysecretpassword psql -h localhost -p 5432 -d mydatabase -U myuser
```