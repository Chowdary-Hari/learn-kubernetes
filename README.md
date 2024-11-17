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
## **----------------------------------------------------------------**
# **create namespace**
```bash
kubectl create namespace < namespace name>
```
::Example::

```bash
kubectl create namespace expense
```

# **get created namespace**
```bash
kubectl get ns  
```
&& 
```bash
kubectl get namespace
```

# **Delete Namespace**
```bash
kubectl delete namespace < namespace name>
```
::Example::

```bash
kubectl delete namespace expense
```


## **----------------------------------------------------------------**

## Example
```yaml
apiVersion: v1
kind: Namespace
metadata:
 name: expense
 labels:
  name: expense
  env: development
```
# create resources
```sh
kubectl apply -f <file-name>.yaml
```
::Example::

```sh
kubectl apply -f namespace.yaml
```

# delete resources 

```sh
kubectl delete -f <file-name>.yaml
```
::Example::

```sh
kubectl delete -f namespace.yaml
```


## **----------------------------------------------------------------**
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