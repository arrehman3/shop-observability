# Low Node Memory

1. Identify the affected node in Grafana.
2. Run `free -h` and `top` on the node.
3. Check Kubernetes usage with `kubectl top pods -A`.
4. Identify memory-heavy workloads.
5. Inspect pod limits and recent deployments.
6. Reduce workload pressure or increase available resources.
7. Verify available memory returns above 15%.
