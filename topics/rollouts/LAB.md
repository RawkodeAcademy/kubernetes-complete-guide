# Guided Lab

- Deploy `nginx:1.22` as a Deployment with 5 replicas on the default rollout strategy.

---
layout: two-cols
---

# Solo Lab

60 minutes

- Upgrade `nginx` to `nginx:1.23` using the `Recreate` rollout strategy
- Upgrade `nginx` to `nginx:1.23` using the `RollingUpdate` rollout strategy with `maxSurge=100%` and `maxUnavailable=50%`
  - Tweak and play with these settings
