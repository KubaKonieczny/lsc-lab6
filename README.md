# lsc-lab6

To run application:

```
minikube start

helm install nfs-server-provisioner nfs-ganesha-server-and-external-provisioner/nfs-server-provisioner  --set storageClass.defaultClass=true  --set storageClass.name=nfs

kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f job.yaml

minikube service l6-service
```
