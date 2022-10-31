# Guided Lab

- N/A

---
layout: two-cols
---

# Solo Lab

40 minutes

- Create an `nginx` pod that has a `liveness` probe that waits for 2xx for `/`
- Create an `nginx` pod that has a `readiness` probe that requires a 200 for `/`
- Create an `nginx` pod that has a `readiness` probe that requires a 200 for `/hello`
  - Make it pass with a ConfigMap
