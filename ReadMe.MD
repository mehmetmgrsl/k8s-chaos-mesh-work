# WIP

### Why do we need chaos-mesh?

To have more robust and reliable systems by identifying weaknesses and vulnerabilities in applications and infrastructure by simulating real-world failures.

### What is chaos-mesh?

A Powerful Chaos Engineering Platform for Kubernetes (1*)

### Precondition

- Kubernetes Cluster

### Installation (2*)

```curl -sSL https://mirrors.chaos-mesh.org/v2.6.2/install.sh | bash``` 

- Verify the installation
```kubectl get po -n chaos-mesh```

```
kubectl get po -n chaos-mesh
NAME                                        READY   STATUS    RESTARTS   AGE
chaos-controller-manager-85bbfb4465-ldt2s   1/1     Running   0          24m
chaos-controller-manager-85bbfb4465-nf7lf   1/1     Running   0          24m
chaos-controller-manager-85bbfb4465-s4jsg   1/1     Running   0          24m
chaos-daemon-8txlg                          1/1     Running   0          24m
chaos-dashboard-68f7cb885f-rtczf            1/1     Running   0          24m
chaos-dns-server-55bd597564-bqv9v           1/1     Running   0          24m
```

### Test (Chaos Experiments)

#### 0. Create example pods
- ```kubectl create ns dev```
- ```kubectl apply -f example-01-deployment.yaml```



#### 1. Simulate Pod Faults


### Uninstall chaos-mesh
```kubectl delete ns chaos-mesh```

### Resources
1*. https://chaos-mesh.org/

2*. https://chaos-mesh.org/docs/quick-start/