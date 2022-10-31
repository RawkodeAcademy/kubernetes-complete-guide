# Guided Lab

Let's create some deployments

- Generate YAML
  - Walkthrough
- Create a `nginx` deployment with `nginx:1.22` image and `1` replica
- Update the image to `nginx:1.23`

---
layout: two-cols
---

# Solo Lab

45 minutes

- Create a deployment called `nginx` that runs the `nginx:1.22` image
- Update deployment to scale to `4` replicas
- Delete all the pods
- How many ReplicaSets do you have?
  - Delete them
- Fix `broken.yaml`
- Create an `alpine` pod with `sleep 3600` command and curl `nginx` from inside it
