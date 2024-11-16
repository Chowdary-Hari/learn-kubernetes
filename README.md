# learn-kubernetes
# **create cluster**

```bash
eksctl create cluster --config-file=<file-name.yml>
```
&&

```bash
eksctl create cluster -f cluster.yaml
```
# **delete create**
```bash
eksctl delete cluster -f cluster.yaml
```
----------------------------------------------------------------
* **display nods in k8 cluster**
```shell
kubectl get nodes
```
* **show version in clint and server**
```shell
kubectl version 
```

* ****
```bash
kubectl get pods 
```

```bash
kubectl apply -f < name >
```

* ****
```bash
kubectl describe pod <name of the pod >
```
:: example ::

```bash
kubectl describe pod nginx
``` 