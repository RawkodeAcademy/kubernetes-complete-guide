---
layout: section
---

# Lab

kubectl

---

# Follow-Along Exercise

Lab: kubectl

In this lab, you will learn:

- How to pronounce `kubectl`
  - `Control`, `C T L`, `cuttle`, `cuddle`
- Logs
- Diff
- Exec
- Debug

---
layout: two-cols
---

# Solo Exercise

Lab: kubectl


- Fix this workload
  - `kubectl apply -f help-me.yaml`

::right::

# Help

Commands You'll Need

**Logs**

```shell
kubectl logs -f pod-name
```

**Exec**

```shell
kubectl exec -it pod-name -- sh
```

**Debug**

```shell
kubectl debug pod_name --target=container-name -it --image=alpine
```
