---
layout: section
---

# Namespaces

---

# Learn

- What is a namespace?
- When do we use namespaces?


---

# Namespace

Namespace: core/v1

Namespaces provide a mechanism for isolating groups of resources within a single cluster. Names of resources need to be unique within a namespace, but not across namespaces.

Namespace-based scoping is applicable only for namespaced objects (e.g. Deployments, Services, etc) and not for cluster-wide objects (e.g. StorageClass, Nodes, PersistentVolumes, etc).

- Quotas, Limits, Network Policies
  - Conway's Law

---
src: ./topics/deployments/LAB.md
---
