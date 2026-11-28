# High Node CPU

1. Identify the affected node in Grafana.
2. SSH into the node.
3. Run `top` or `htop` to identify CPU-heavy processes.
4. Check Kubernetes workloads using `kubectl top pods -A`.
5. Inspect recent deployments and workload activity.
6. Scale or restart the affected workload if necessary.
7. Verify CPU usage returns below 80%.
