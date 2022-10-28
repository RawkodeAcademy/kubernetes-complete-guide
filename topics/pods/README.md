---
layout: section
---

# Pods

---

# Learn

- What's a Pod?
- CRUD
- Get Vs. Describe
- Exporting to YAML
- How to access a pod's application with port-forwarding
- Explain

---
layout: header-two-cols
---

# Pod

Namespace: core/v1

One or more container that, can, share some namespaces:

::left::

- Network
  - Only a single IP address is allocated to a pod
  - As such, port / bind space is shared
  - Localhost
- UTS
  - Hostname
- IPC
  - Inter Process Communication (POSIX shared memory and semaphores)

::right::

- Process (Sometimes)
  - PID 1
- Mount
  - Volumes
  - Root filesystems **ARE NOT** shared

---
src: ./topics/pods/LAB.md
---

---
src: ./topics/pods/QUIZ.md
---
