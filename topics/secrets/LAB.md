# Guided Lab

Let's create some Secret's

- Generate YAML
  - Walkthrough (As much as I can at-least)
  - There's no escaping the YAML
- Store the key-value pair `abc=123` in the Secret

---
layout: two-cols
---

# Solo Lab

20 (10?) minutes

- Create a Secret with the following key-value pairs: `abc=123` and `def=xyz`
- Expose the entire Secret as environment variables on a Pod
- Confirm it works with `kubectl logs -f secret-example`
