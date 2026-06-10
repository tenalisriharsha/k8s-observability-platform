<<<<<<< HEAD
# k8s-observability-platform
=======
# K8s Observability Platform

Learning log for SRE / Platform Engineering transition.

## Day 1: Minikube + Nginx Deployment
- Installed kubectl (v1.36.1) and minikube (v1.38.1) via Homebrew on Mac Studio
- Started local cluster with Docker driver
- Deployed nginx via declarative YAML with 3 replicas
- Verified Deployment → ReplicaSet → Pod hierarchy
- Exposed service via NodePort and accessed via browser tunnel

### Key Commands
kubectl apply -f nginx-deployment.yaml
kubectl get deployments,replicasets,pods
minikube service nginx
>>>>>>> 11ae3f8 (day-1: minikube nginx deployment with 3 replicas)

## Day 2: Services & ConfigMaps
- Rebuilt deployment declaratively with resource limits (CPU/memory)
- Added ConfigMap to serve custom HTML content
- Created Service YAML with ClusterIP, NodePort, and LoadBalancer types
- Mastered kubectl port-forward for local debugging
- Verified 3 replicas running with custom content mounted via volume
