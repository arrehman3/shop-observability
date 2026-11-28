# Shop Pod Failure

1. Run `kubectl get pods -n shop -o wide`.
2. Identify pods in Pending, Failed or Unknown states.
3. Run `kubectl describe pod <pod> -n shop`.
4. Inspect namespace events with `kubectl get events -n shop --sort-by=.lastTimestamp`.
5. Check image, scheduling, storage and resource issues.
6. Apply the required fix and restore the affected workload.
7. Verify all Shop pods are Running.
