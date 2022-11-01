# Solo Lab

60 minutes

- Deploy `nginx`
- Create a `NetworkPolicy` that allows traffic to `nginx` from pods with the label `http=hell-yeah`
- Create a pod with the label `http=hell-yeah` and verify that it can access nginx
    - Confirm that other pods cannot access nginx
