# Container Restarts

1. Identify the affected pod in Grafana.
2. Run `kubectl get pods -n shop`.
3. Inspect the pod using `kubectl describe pod <pod> -n shop`.
4. Check current and previous container logs.
5. Inspect events for OOMKilled, probe failures or crashes.
6. Fix the underlying configuration or resource issue.
7. Verify the restart count stops increasing.
