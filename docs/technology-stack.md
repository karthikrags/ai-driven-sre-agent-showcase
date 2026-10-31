# Technology stack

| Area | Technologies and role |
| --- | --- |
| Cluster | Kubernetes / OpenShift for the demonstration workloads and APIs |
| Monitoring | Prometheus, Prometheus Operator rules, Alertmanager webhooks |
| Orchestration | OpenClaw with a configured LLM provider |
| Evidence | Kubernetes MCP server with allowlisted reads and Markdown RAG retrieval |
| Workflow | Slack Bolt / Socket Mode for investigation, proposal, approval, and outcomes |
| Remediation | Python/FastAPI service, SQLite lifecycle/audit persistence, policy and action catalog, Kubernetes server-side dry-run |
| User interface | Preact and Vite Command Center backed by a read-only observation API |
| Packaging | Docker images and Kubernetes manifests |

Names describe the implementation used in the demonstration; deployment specifics are intentionally omitted from this public overview.
