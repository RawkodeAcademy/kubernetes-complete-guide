# Guided Lab

Let's create some pods

- Generate YAML
  - Walkthrough
- Create a `hello-world` Pod
  - Logs
  - Get
  - Describe
  - Delete
- Create a `functions/nodeinfo` Pod
  - Port-forward to the pod and access the application
- Create a `alpine` pod with `sleep 3600` command
  - Exec into the pod and run `ls -la /` and `ps -auxef`

---
layout: two-cols
---

# Solo Lab

20 minutes


- Create a Pod named `nginx` that runs the `nginx:1.22` image
- Port-forward to access your nginx pod
- View the logs for your nginx pod
- Upgrade your nginx pod to `nginx:1.23`
- Delete your nginx pod
- Create a Pod named `echo` that runs the `alpine` image
  - Set the command and arguments so that the pod runs `echo "Hello World" && env`

If there's any rate limiting, use the GCR or ECR mirrors:

- public.ecr.aws/docker/library/nginx:latest
- mirror.gcr.io/library/nginx:latest

::right::

# Help

Useful Commands

**Create a Resource**

```shell
kubectl apply -f manifest.yaml
```

**Delete a Resource**

```shell
kubectl delete -f manifest.yaml
kubectl delete pod name
```

**Exporting to YAML**

```shell
kubectl get pod name -o yaml > pod.yaml
```


**Port-Forwarding**

```shell
kubectl port-forward pod/name local_port:container_port
```

---

# Tips

Kubectl Tricks

- You can query multiple resources at the same time: `kubectl get nodes,pods,services`
- You can use short-hand names for resources: `kubectl get no,po,svc`
- You can discover these short-hands, and more, with `kubectl api-resources`
