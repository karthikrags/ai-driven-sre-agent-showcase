# Demonstration guide

## Walkthrough

1. Start with a healthy, isolated scenario workload and its Prometheus rule.
2. Introduce one documented fault using the lab operator workflow. Alert on the resulting failure and follow its Alertmanager notification to the SRE Alert Receiver.
3. Review the incident and the OpenClaw investigation. Inspect the read-only Kubernetes evidence and retrieved RAG references; distinguish observations from hypotheses.
4. In Slack, use **Remediate** to request a proposal. Review the selected action, policy scope, and server-side dry-run result. At this point the cluster has not been changed by proposal preparation.
5. A human approver reviews the bound Slack card and chooses **Approve & Execute** or **Reject**. Never treat an AI recommendation as an approval.
6. Review the Slack execution outcome, audit, recovery checks, incident lifecycle, and read-only SRE Ops Dashboard (Command Center) view.
7. If rollback is needed and eligible, prepare the separate snapshot-based proposal and require a new authenticated approval. Confirm workload health independently after restoration.

## Presentation materials

- [Eight-stage flow](architecture/incident-response-flow.png)
- [Detailed system architecture](architecture/system-architecture.png)
- [Technical component flow](architecture/technical-component-flow.png)
- [Synthetic Command Center screenshot](assets/screenshots/command-center-synthetic.png)

The screenshot is a constructed illustration with fictional values. No live dashboard capture or private runtime data is included.
