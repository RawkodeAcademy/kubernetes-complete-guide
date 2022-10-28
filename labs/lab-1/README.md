---
layout: section
---

# Lab

Pods

---

# Follow-Along Exercise

Lab: Pods

In this lab, you will learn:

- What's a Pod?
- CRUD
- Get Vs. Describe
- Exporting to YAML
- How to access a pod's application with port-forwarding
- Explain

---
layout: two-cols
---

# Solo Exercise

Lab: Pods


- Create a pod named `nginx` that runs the latest `nginx` image
- Create a pod named `nginx` that runs the latest `nginx` image

If there's any rate limiting, use the GCR or ECR mirrors:

- public.ecr.aws/docker/library/nginx:latest
- mirror.gcr.io/library/nginx:latest

::right::

# Help

Commands You'll Need

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
