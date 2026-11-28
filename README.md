# Online Boutique - End-to-End Observability

## Overview
Deployed Google's Online Boutique microservices application on Kubernetes and implemented infrastructure monitoring, Kubernetes monitoring, centralized logging, dashboards and alerting.

## Architecture

### Application
- Google Online Boutique microservices
- Kubernetes cluster (control plane and worker)
- Nginx reverse proxy on a separate EC2 instance
- Frontend exposed through NodePort

### Monitoring
- Prometheus for metrics collection
- Grafana for dashboards and alerting
- Node Exporter for host metrics
- cAdvisor for container metrics
- kube-state-metrics for Kubernetes metrics

### Logging
- Fluent Bit for log collection
- Elasticsearch for centralized log storage
- Nginx access and error logs
- Linux systemd logs
- Kubernetes container logs
- Kibana dashboards skipped due to resource constraints

## Grafana Dashboards
1. Shop Infrastructure Monitoring
2. Shop Kubernetes Workloads

## Alert Rules
1. Shop - High Node CPU
2. Shop - Low Node Memory
3. Shop - Container Restarts
4. Shop - Pod Failure
5. Shop - Frontend Unavailable

## Elasticsearch Retention
- Nginx logs: 90 days
- Kubernetes logs: 14 days
- System logs: 14 days

## Runbooks
Five operational runbooks are available under `runbooks/`.

## Incident Validation

### High CPU Incident
- Deployed a temporary CPU-intensive pod.
- Observed increased CPU utilization.
- Grafana successfully triggered the High Node CPU alert.
- Removed the stress pod.
- Confirmed CPU utilization decreased.

Other planned incident drills were skipped.

## Repository Structure

- `app-vm/` - Nginx and application VM configuration
- `kubernetes/` - Online Boutique Kubernetes manifests
- `monitoring/` - Prometheus and Grafana configuration
- `logging/` - Fluent Bit and Elasticsearch configuration
- `runbooks/` - Operational troubleshooting guides

## Technologies
AWS EC2, Ubuntu, Docker, Kubernetes, Nginx, Prometheus, Grafana, Node Exporter, cAdvisor, kube-state-metrics, Fluent Bit and Elasticsearch.

## Security
Never commit passwords, private keys, access tokens or other secrets.
