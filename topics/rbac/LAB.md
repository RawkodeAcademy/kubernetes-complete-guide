# Guided Lab

- Use `kubectl` with default service account

---
layout: two-cols
---

# Solo Lab

40 minutes

- Create a `ServiceAccount` called `workshop`
- Create a `Role` called `workshop`
  - Ensure this role can list all pods in the current namespace
  - Ensure this role can list all deployments in the current namespace
- Create a `ClusterRole` called `workshopc`
  - Ensure this role can list all pods in all namespaces
