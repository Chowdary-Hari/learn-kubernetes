# **1. Set `expense` Namespace as Default for the Current Context**

```bash
kubectl config set-context --current --namespace=expense
```


### **2. Verify the Change**

```bash
kubectl config view --minify | grep namespace:
```

The output should be:

```plaintext
namespace: expense
```

### **3. List Pods in the `expense` Namespace**

```bash
kubectl get pods
```


### **4. Temporarily Switch to `expense` Namespace (Optional)**

```bash
kubectl get pods -n expense
```