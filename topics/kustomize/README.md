---
layout: section
---

# Kustomize

---

# Learn

- What is Kustomize?
- Why Kustomize?

---
layout: header-two-cols
---

# Kustomize

From: Google / CNCF / Kubernetes

Kustomize is a Kubernetes native tool that allows you to customize raw, template-free YAML files for multiple purposes, leaving the original YAML untouched and usable as is.

Let's us transform resources: A->B->C

Supports overlays and patches

---

# Example

```yaml
apiVersion: kustomize.config.k8s.io/v1beta1
kind: Kustomization
commonAnnotations:
  environment: production-always
commonLabels:
  i-know: what-im-doing
namePrefix: production-
patchesStrategicMerge:
- production-hpa.yaml
bases:
- base/
resources:
- ingress.yaml
- permissions.yaml
configMapGenerator:
- name: config
  files:
  - app.conf
```

---
src: ./topics/kustomize/LAB.md
---
