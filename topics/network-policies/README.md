# Network Policies

Namespace: networking.k8s.io/v1

Network Policies are a way to control the traffic to pods within a cluster.

Want to block all egress? Need to restrict ingress to a certain namespace, or label selector? NetPol's.

---

# Flavours

While `networking.k8s.io/v1` provides basic NetworkPolicies, each CNI implementation has its own flavour.

---
src: ./topics/network-policies/LAB.md
```
