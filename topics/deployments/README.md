---
layout: section
---

# Deployments

---

# Learn

- What is a deployment?
- Why do we need deployments?
- How Kubernetes controllers work in practice


---
layout: header-two-cols
---

# Deployment

Namespace: apps/v1

A deployment is a resource that can be updated at will and the controllers will ensure we have a healthy rollout of said changes with the ability to orchestrate more advanced deployment mechanisms, such as blue/green.

::left::

- Pods will be created for us
  - Oh, and ReplicaSets too 😀
- Their health is monitored and they're replaced if needed
- Can be scaled up and down
- Not immutable like our pod-friend

::right::

- Rollout strategies can be configured
- Multiple versions of our application can be active
- The de-facto way to deploy stateless applications to Kubernetes
- Labels are very important

---
src: ./topics/deployments/LAB.md
---

---
src: ./topics/deployments/quiz.md
---