# Project overview

The AI-Driven SRE Agent joins Kubernetes monitoring, read-only investigation, policy-bounded remediation preparation, authenticated Slack approval, controlled recovery, and an audit-backed read-only SRE Ops Dashboard (Command Center).

## Services

- **Prometheus + Alertmanager:** evaluate configured rules and send firing-alert webhooks.
- **SRE Alert Receiver:** validate, normalize, correlate, and forward alert context.
- **OpenClaw:** coordinate investigation and the configured LLM interaction.
- **Kubernetes MCP:** expose scoped read operations and RAG search to the investigation.
- **Remediation API / execution service:** validate policy, prepare server-side dry-runs, bind approval, execute only an approved operation, verify, and persist lifecycle/audit state.
- **Slack:** present investigation, Remediate, proposal review, authenticated approval or rejection, and outcome interactions.
- **SRE Ops Dashboard (Command Center):** display token-scoped observations without direct cluster or database access.

## Evidence and limits

The architecture is based on the private source snapshot and sanitized validation reports. Recorded evidence includes all 20 scenario alert/investigation paths and selected live approved remediation and rollback exercises. It does not imply every scenario has a completed live remediation path. The [architecture guide](architecture/system-architecture.png) and [data-flow diagram](architecture/technical-component-flow.png) distinguish observation from controlled writes.
