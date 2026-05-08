# ☸️ Kubernetes Short Revision Notes (Interview Ready)

Using Kubernetes

---

# 1. What is Kubernetes?

## Definition

Kubernetes is a container orchestration platform used to deploy, manage, scale, and automate containerized applications.

## Simple Words

👉 Kubernetes manages Docker containers automatically.

---

# 2. Why Kubernetes is used

* Auto scaling
* Self-healing
* Load balancing
* Automatic deployment
* High availability

---

# 3. Kubernetes Architecture

```text id="h4d8x2"
Control Plane (Master)
        ↓
Worker Nodes
        ↓
Pods
```

---

# 4. Pod

## Definition

Pod is the smallest deployable unit in Kubernetes.

## Simple Words

👉 Pod contains one or more containers.

---

# 5. Deployment

## Definition

Deployment manages pods and ensures desired number of pods are running.

## Uses

* Scaling
* Rolling updates
* Auto restart

---

# 6. ReplicaSet

## Definition

ReplicaSet maintains the required number of pod replicas.

## Example

```yaml id="p25bmh"
replicas: 3
```

---

# 7. Service

## Definition

Service provides stable network access to pods.

## Types

* ClusterIP
* NodePort
* LoadBalancer

---

# 8. Namespace

## Definition

Namespace is used to logically separate Kubernetes resources.

---

# 9. ConfigMap

## Definition

ConfigMap stores non-sensitive configuration data.

---

# 10. Secret

## Definition

Secret stores sensitive data like passwords and API keys.

---

# 11. Ingress

## Definition

Ingress manages external HTTP/HTTPS traffic to services.

---

# 12. kubectl

## Definition

kubectl is the command-line tool used to interact with Kubernetes clusters.

---

# 13. Scaling

## Definition

Scaling means increasing or decreasing the number of pods based on traffic.

---

# 14. Self-Healing

## Definition

Kubernetes automatically recreates failed containers or pods.

---

# 15. Rolling Update

## Definition

Rolling update updates application pods gradually without downtime.

---

# 16. Load Balancer

## Definition

Load balancer distributes traffic across multiple pods or servers.

---

# 17. Docker vs Kubernetes

| Docker                 | Kubernetes                    |
| ---------------------- | ----------------------------- |
| Creates containers     | Manages containers            |
| Single container focus | Multi-container orchestration |

---

# 18. Deployment YAML Example

```yaml id="d1lqhk"
apiVersion: apps/v1
kind: Deployment

metadata:
  name: nginx-deployment

spec:
  replicas: 2

  selector:
    matchLabels:
      app: nginx

  template:
    metadata:
      labels:
        app: nginx

    spec:
      containers:
      - name: nginx
        image: nginx
```

---

# 19. Service YAML Example

```yaml id="p82we7"
apiVersion: v1
kind: Service

metadata:
  name: nginx-service

spec:
  type: NodePort

  selector:
    app: nginx

  ports:
    - port: 80
      targetPort: 80
```

---

# 20. Important kubectl Commands

## Get Pods

```bash id="fpp7w0"
kubectl get pods
```

---

## Get Services

```bash id="iq2xw7"
kubectl get services
```

---

## Apply YAML

```bash id="1z0otk"
kubectl apply -f file.yml
```

---

## Delete Resource

```bash id="i6kuyz"
kubectl delete -f file.yml
```

---

## Pod Logs

```bash id="r9lsy3"
kubectl logs pod-name
```

---

# 21. Important Interview One-Liners

## Kubernetes

Platform used to automate deployment and management of containers.

---

## Pod

Smallest deployable unit in Kubernetes.

---

## Deployment

Manages pods and updates.

---

## Service

Provides stable communication for pods.

---

## ReplicaSet

Maintains desired number of pods.

---

## Ingress

Controls external web traffic.

---

## kubectl

CLI tool for Kubernetes.

---

# 22. Super Short Flow

```text id="3y6kmt"
Docker Image
      ↓
Pod
      ↓
Deployment
      ↓
Service
      ↓
Users access app
```

---

# 🎯 Final One-Line Summary

**Kubernetes is used to automatically deploy, manage, scale, and monitor containerized applications in production environments.**
