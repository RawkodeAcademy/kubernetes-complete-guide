---
theme: seriph
layout: cover
background: cover.jpg
themeConfig:
  primary: '#00CEFF'
highlighter: shiki
lineNumbers: true
info: |
  ## Kubernetes Workshop
  by David Flanagan / @rawkode
drawings:
  persist: false
css: unocss
title: Hands-on Introduction to Kubernetes
---

# Introduction to Kubernetes

## David Flanagan

### <carbon-logo-twitter /> rawkode

---

# Our Objectives for Today

## Understand the following

1. Kubernetes Control Plane
2. Kubernetes Primitives
3. Operating Stateful Workloads
4. Multi-Container Patterns

---

# How We Attain Them

1. Hands-on
2. Learn How to Learn
3. Ask Questions

---

# Setting Some Norms

1. I Don't Know
2. I Don't Understand

---

# What is Kubernetes?

Kubernetes, commonly stylized as K8s, is an open-source container orchestration system for automating software deployment, scaling, and management. Google originally designed Kubernetes, but the Cloud Native Computing Foundation now maintains the project.

## What does this mean?

- Manage containers across multiple hosts
- Ensure those containers are running correctly
- Ensure those containers can work together as a single unit.
- Allow those containers can scale independently
- Enforce CPU and memory constraints for applications
- ~~Run containers securely~~

---

# How does it work?

Declarative Configuration

- We describe Kubernetes resources in YAML
- Kubernetes has "controllers" that monitor for changes and "reconcile"
- Kubernetes is **eventually consistent**
  - Eventually consistent sometimes means never consistent
- "Simple" CRUD API

---

# Kubernetes Control Plane

Kubernetes is a distributed system for running distributed systems

## Control Plane

- API Server
- Controller Manager
- Scheduler

## Worker Plane

- Kubelet
- Container Network Interface
- Container Runtime Interface
- Container Storage Interface

---
layout: cover
background: https://64.media.tumblr.com/00d64c8e43cdd38883ab26ed7926f2c3/7a5e3920b4ee99e0-f6/s540x810/def30630aeebce028668834bb15d2e8a41ca70f4.gif
---
# We don't talk about etcd

---

# API Server

How we communicate with Kubernetes

Everytime you run a `kubectl` command, you're communicating directly with the Kubernetes API server.

It takes your instructions and:

1. writes the desired state to etcd.
2. reads from etcd

---

# Controller Manager / Controllers

Controller Manager is a supervisor for many other controllers

Everytime the desired state is modified in etcd, events are emitted and picked up by the controllers.

They're state machines that work out what needs to happen for the desired state to be realised.

---

# Scheduler

Where should we run our workloads?

Whenever our desired state changes and we need a new pod to be created, the scheduler is responsible for decided where that pod should run.

Things that can influence where a pod will be scheduled include, but not limited to:

- CPU / Memory constraints
- Node topology
- Architecture
- Storage and HDD/SSD classes
- Taints and tolerations
- More!

---

# Kubelet

Let's get to work!

Once something is scheduled, we need that workload to be created on the node.

The Kubelet is a process that runs on every node within your cluster and handles all that plumbing.

- Works with CNI to create IP address
- Works with CSI to provision any volumes
- Works with the CRI to create containers
- Responsible for running container based checks
- Responsible for ensuring containers are restarted should they fail checks


---

# Pods

- Share network namespace
  - IP address / binds
- Share PID namespace
  - PID 1
- Share mount namespace
  - volumes

---
src: ./labs/lab-1/README.md
---

---
src: ./labs/lab-2/README.md
---
