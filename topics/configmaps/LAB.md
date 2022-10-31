# Guided Lab

Let's create some ConfigMap's

- Generate YAML
  - Walkthrough (As much as I can at-least)
  - There's no escaping the YAML
- Store the key-value pair `abc=123` in the ConfigMap

---
layout: two-cols
---

# Solo Lab

30 minutes

- Create a ConfigMap with the following key-value pairs: `abc=123` and `def=xyz`
- Add the `data.json` file to the ConfigMap
- Expose the entire ConfigMap as environment variables on a Pod
- Confirm it works with `kubectl logs -f configmap-example`
- Fix `broken.yaml`
