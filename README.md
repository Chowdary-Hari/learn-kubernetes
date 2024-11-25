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
************************************************************************************************
# **create namespace**
```bash
kubectl create namespace < namespace name>
```
::Example::

```bash
kubectl create namespace expense
```
# Set the Namespace for the Current Context

```shell
kubectl config set-context --current --namespace=<namespace-name>
```

# Verify the Configuration

```shell
kubectl config view --minify | grep namespace:
```
---


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


************************************************************************************************

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

## delete pod && running containers 
```bash
kubectl delete pod expense
```

************************************************************************************************
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
************************************************************************************************

# **connect running container**
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: expense
  namespace: expense
spec:
  containers:
    - name: nginx
      image: nginx:latest
      ports:
        - containerPort: 80
    - name: tomcat
      image: tomcat:latest
      ports:
        - containerPort: 8080
```


```bash
kubectl exec -it nginx -c nginx -- bash
```
- `nginx`: This is the **name of the pod** you're targeting. Replace it with your actual pod name if different.

- If the pod only has one container, you can simplify the command to:

```bash
kubectl exec -it nginx -- bash
```


```shell
(base) ➜  notebook git:(main) git reset --hard 
(base) ➜  notebook git:(main) git clean -fd 
```
```shell
echo "alias k='microk8s kubectl'" >> ~/.zshrc
```
pod is a subset of replicaset
replicaset  subset of a deployment

cluster ip << node port << loadbalancing  > Service

container <<::pod << replicaset << deployment 

pod to pod comunation can be achive thre the service it is loadbalancing all so. > Service    