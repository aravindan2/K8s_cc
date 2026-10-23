# Cloud Computing — Assignment 2
## Project Files

| File | Description |
|---|---|
| `flask_app/` | Flask application source code, Dockerfile, and dependencies. |
| `docker-compose.yaml` | **Part 2:** Runs Flask and MongoDB locally in separate Docker containers, with a bind mount for MongoDB persistence. |
| `k8s.yaml` | **Part 3:** Original Kubernetes configuration for deploying Flask and MongoDB on Minikube. |
| `flask-service.yaml` | **Part 3:** Exposes the Flask application using a NodePort Service. |
| `gke.yaml` | **Parts 4–7:** Final GKE configuration, including the LoadBalancer Service, replicas, rolling update strategy, and liveness/readiness probes. |
| `gke-part6-backup.yaml` | Backup of the deployment configuration before Part 6 changes. |
| `gke-healthy.yaml` | Working configuration used to restore the application after health probe failure tests in Part 7. |
| `gke-before-alert-test.yaml` | Backup used to restore the application after triggering Prometheus alerts in Part 8. |
| `prometheus-values.yaml` | **Part 8:** Helm configuration for Prometheus, Alertmanager, and Slack integration. |
| `prometheus-alerts.yaml` | **Part 8:** Prometheus alert rule (`FlaskPodNotReady`) for detecting unhealthy Flask pods. |

## Notes

- `gke.yaml` is the final Kubernetes configuration.
- The backup YAML files are retained for reference and testing.
- The GKE cluster was deleted after completing the assignment to avoid ongoing cloud charges.
- Slack webhook credentials are stored separately as Kubernetes Secrets and are not included in this repository.