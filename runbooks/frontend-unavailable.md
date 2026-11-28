# Frontend Unavailable

1. Run `kubectl get pods -n shop -l app=frontend`.
2. Inspect frontend pod events and logs.
3. Check the frontend service and endpoints.
4. Test the NodePort on the worker: `curl http://172.31.41.100:30080`.
5. Check Nginx on the App VM at 172.31.43.104.
6. Restore the frontend pod or correct the service/proxy configuration.
7. Verify the public website at http://13.51.196.249.
