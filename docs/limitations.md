# Limitations and future work

## Current limits

- This is an educational demonstration, not production certification or a recommendation for unattended remediation.
- LLM output can be incomplete or wrong. Evidence collection can be unavailable, and findings must retain uncertainty and provenance.
- Read-only investigation and selected live approval/execution paths have been demonstrated; every scenario has not been validated through remediation.
- A rollback can restore configuration without restoring workload health. Verification must check the application separately.
- Monitoring rules, resource scopes, image references, LLM provider, Slack identity, credentials, and service endpoints require environment-specific setup.
- The public showcase contains diagrams and sanitized summaries only; it does not provide a runnable application.

## Future work

- Expand repeatable, scenario-specific validation for proposal, dry-run, approval, execution, verification, and audit.
- Improve reproducible deployment, image provenance, signing, dependency pinning, and software bill of materials.
- Add additional environment-specific operational and failure-injection guidance after security review.
