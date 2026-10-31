# Security architecture

## Read-only investigation

OpenClaw invokes the Kubernetes MCP service for allowlisted evidence collection. Its investigation role is read-only and separate from the remediation execution identity. The SRE Ops Dashboard (Command Center) uses a distinct token-scoped observation API and has neither Kubernetes credentials nor direct database access. Slack carries the investigation and the separately authenticated approval workflow.

## Controlled write path

Proposal preparation validates an allowlisted action, target scope, and policy, then performs Kubernetes server-side dry-run. It persists a reviewable candidate/proposal but performs no cluster write. The exact proposal is bound to its Slack review interaction.

An authenticated human approval is required for execution. Expiration, actor/message binding, one-time authorization, replay defenses, revalidation of the target operation, and scoped RBAC constrain the write. The execution service snapshots the relevant pre-change state, records audit events, and verifies the result.

Rollback uses an eligible snapshot through a separate proposal and separate authenticated approval. Restoration and health verification are separate outcomes; a restored configuration may not recover a workload.

## Data excluded from this showcase

This repository is a documentation-only showcase. It contains no application implementation, credential values, private endpoints, kubeconfigs, live incident databases, private audit logs, VM images, or raw runtime evidence. The sample screenshot uses wholly synthetic labels and values.
