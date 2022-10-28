# Jobs

Namespace: batch/v1

For short-term workloads, we can leverage the various job resources.

## Types of Jobs

- batch/v1/Job
- batch/v1/CronJob

---

# Jobs

For short-term workloads, we can leverage the various job resources.

## Job

Jobs are pods that run until completion. Unlike a plain pod, if the job pod fails it will be retried within the constraints of the configuration.

## CronJob (cj)

CronJob's are just as you'd expect. These are jobs that are scheduled to run at specific times, using the syntax we all love and hate.

Remember, [CronTab.guru](https://crontab.guru/) is your friend.

---
src: ./topics/jobs/LAB.md
---
