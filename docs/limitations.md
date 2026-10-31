# Limitations and future work

## Current limits

- This is an educational demonstration, not production certification or a recommendation for unattended remediation.
- LLM output can be incomplete or wrong. Evidence collection can be unavailable, and findings must retain uncertainty and provenance.
- Read-only investigation and selected live approval/execution paths have been demonstrated; every scenario has not been validated through remediation.
- A rollback can restore configuration without restoring workload health. Verification must check the application separately.
- Monitoring rules, resource scopes, image references, LLM provider, Slack identity, credentials, and service endpoints require environment-specific setup.
- The public showcase contains diagrams and sanitized summaries only; it does not provide a runnable application.

## Future work

- Build a RAG MLOps pipeline for automated document ingestion, validation, versioning, and retrieval-quality testing.
- Extend the single-environment design to multi-cluster operation with explicit tenant/cluster scope, per-cluster identities, and separate policy review.
- Expand the existing allowlisted remediation catalog with low-risk SOP actions while retaining dry-run and authenticated human approval.
- Add a reviewed incident-learning loop that curates sanitized RCAs and outcomes into RAG with provenance and quality checks.
- Extend duplicate suppression into explainable correlation of related alerts.
- Add advisory predictive SRE signals for drift, capacity, certificate expiry, and failure trends; keep the existing approval boundary for writes.
- Expand scenario-specific end-to-end validation, deployment reproducibility, image provenance, signing, dependency pinning, and SBOM generation.
