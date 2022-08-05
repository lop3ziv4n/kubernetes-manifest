# Kubernetes:
- manifest --> deployment (yaml)
- etcd
- controllers
- cluster --> node --> workers --> pod --> container 

## Services:
- load balancer
- ingress
- cluster ip
- node port

## Master:
- API Server
- Controller Manager
- Scheduler 

## Versions:
### Local:
- k3s (https://k3s.io/) (For low-end PCs)
- Minikube (https://minikube.sigs.k8s.io/docs/)
- kind (https://kind.sigs.k8s.io/)
- Microk8s (https://microk8s.io/)
### Providers without kubernetes:
- k0s (https://docs.k0sproject.io/v1.23.6+k0s.2/) 

## Use MicroK8s Kubernetes
### start process
> sudo microk8s start
### create the environment 
> sudo microk8s kubectl apply -f <your-configmap>.yaml
### create the persistent volume 
> sudo microk8s kubectl apply -f <your-pv>.yaml
### create the persistent volume 
> sudo microk8s kubectl apply -f <your-pv-claim>.yaml
### create the deployment 
> sudo microk8s kubectl apply -f <your-deployment>.yaml
### create the service 
> sudo microk8s kubectl apply -f <your-service>.yaml
### create the endpoint 
> sudo microk8s kubectl apply -f <your-endpoint>.yaml

### get deployments, pods and services
> sudo microk8s kubectl get deployments

> sudo microk8s kubectl get pods

> sudo microk8s kubectl get services

> sudo microk8s kubectl get endpoints

### delete 
> sudo microk8s kubectl delete service <your-service>

> sudo microk8s kubectl delete deployment <your-deployment>

> sudo microk8s kubectl delete configmap <your-configmap>

> sudo microk8s kubectl delete persistentvolumeclaim <your-pv-claim>

> sudo microk8s kubectl delete persistentvolume <your-pv>

### service
> sudo microk8s kubectl describe services <your-service>

> sudo microk8s kubectl get ep <your-service>

### secret docker image pull
> sudo microk8s kubectl create secret docker-registry flenicred --docker-server=<your-registry-server> --docker-username=<your-name> --docker-password=<your-pword> --docker-email=<your-email>
