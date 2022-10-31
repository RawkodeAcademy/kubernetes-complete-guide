---
layout: section
---

# Volumes

---

# Learn

- What are volumes used for in Kubernetes?
- New ways to consume a ConfigMap's and Secrets

---

# Volumes

Namespace: N/A

A volume in Kubernetes is much like a volume, partition, or directory on the Linux filesystem.

You can use `emptyDir` volumes for scratch / ephemeral storage within pods, but you can also use existing objects (ConfigMaps and Secrets) as projection volumes.

These are not their own resources and are tied exclusively to their parent resource.

# PersistentVolumes

Namespace: core/v1

A PersistentVolume (PV) in Kubernetes is a piece of storage in the cluster that has been provisioned by an "administrator".

It is a resource in the cluster just like a node, pod, deployment, and everything else ... A slice of YAML, if you will.

PVs are just like regular volumes, but have their own lifecycle.

---
src: ./topics/volumes/LAB.md
---
