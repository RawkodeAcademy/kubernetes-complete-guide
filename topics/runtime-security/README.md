---
layout: section
---

# Runtime Security

---

# Learn

- What is Runtime Security?
  - Seccomp
  - Capability
  - Namespaces

---

# RuntimeDefault

Namespace: core/v1

Runtime Security is a feature of Kubernetes that allows you to restrict the capabilities of a container. It is enabled by default, but can be disabled by setting `runtimeClassHandler` to `unconfined`. However, this is not recommended.

The capabilities of a container can be restricted by setting `runtimeClassHandler` to `runtime/default`.

This will restrict the capabilities of a container to the following: `CAP_CHOWN`, `CAP_DAC_OVERRIDE`, `CAP_FOWNER`, `CAP_FSETID`, `CAP_KILL`, `CAP_SETGID`, `CAP_SETUID`, `CAP_SETPCAP`, `CAP_NET_BIND_SERVICE`, `CAP_NET_RAW`, `CAP_SYS_CHROOT`, `CAP_MKNOD`, `CAP_AUDIT_WRITE`, `CAP_SETFCAP`.

Useful, right? Try `apk add --update libcap && capsh --print`

---
src: ./topics/runtime-security/LAB.md
---
