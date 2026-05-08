## kubectl version --client

## kubectl get nodes

## cluster = collection of multiple nodes

## Kuberenetes Architecture - 
## control Plane (Master)- API server, Schedular, etcd

## kubectl get pods --all-namespaces

## Pods - Smallest deployable unit in Kubernetes. (It is temporary)

## kubectl apply -f my-pod.yaml

## kubectl get pods

## kubectl delete pod my-first-pod

## kubectl apply -f nginx-deployment.yaml

## kubectl get deployment

## kubectl scale deployment nginx-deploy --replicas=5m

## Control Plane (Master Node)
Controls whole cluster.
Main components:-
Component	          Work
API Server -          Entry point
Scheduler -	          Decides where pods run
Controller Manager -  Maintains desired state
etcd -                Stores cluster data


## Important Interview One-Liners
Pod - Smallest deployable unit in Kubernetes.

Deployment - Manages pods and updates.

Service - Provides stable network access to pods.

ReplicaSet - Maintains desired number of pods.

kubectl - CLI tool for Kubernetes.

Ingress - Controls external traffic.

## Services - 

kubectl apply -f nginx-deployment.yaml

kubectl apply -f nginx-service.yaml

kubectl get svc

kubectl port-forward deployment/nginx-deploy 8082:80

kubectl port-forward deployment/nginx-deploy 8082:80 8083:80 8084:80

## Namespace - 

Kubernetes already gives some: -
default -> where your apps go (by default)
kube-system	-> system components
kube-public	-> public resources
kube-node-lease	-> node heartbeat

# kubectl get namespaces

# kubectl create namespace dev-environment

# kubectl get namespaces

# kubectl apply -f nginx-deployment.yaml -n dev-environment

# kubectl get pods 

# kubectl get pods -n dev-environment
