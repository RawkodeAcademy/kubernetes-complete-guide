---
layout: section
---

# Downward API

---

# Learn

- What is the Downward API?

---

# Downward API

Expose "internal" info

It is sometimes useful for a container to have information about itself, without being overly coupled to Kubernetes. The downward API allows containers to consume information about themselves or the cluster without using the Kubernetes client or API server.

An example is an existing application that assumes a particular well-known environment variable holds a unique identifier. One possibility is to wrap the application, but that is tedious and error-prone, and it violates the goal of low coupling. A better option would be to use the Pod's name as an identifier, and inject the Pod's name into the well-known environment variable.

The law-of-demeter is watching you.

---
src: ./topics/downward-api/LAB.md
---
