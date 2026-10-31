# Twenty demonstration scenarios

Scenarios illustrate how distinct Kubernetes failure signals can be detected and investigated. They are demonstration examples, not claims that each scenario has a verified live remediation.

| ID | Failure class | Example evidence |
| --- | --- | --- |
| S01 | Image pull failure | Pod events and image status |
| S02 | Invalid startup command | Container start failure |
| S03 | Readiness probe failure | Probe condition and response |
| S04 | Service selector mismatch | Missing ready endpoints |
| S05 | Memory limit / OOM termination | Container termination and memory evidence |
| S06 | CPU throttling | Resource metric evidence |
| S07 | Load and bounded scale-out | Load and replica comparison |
| S08 | Unschedulable resource request | Scheduler event |
| S09 | Invalid ConfigMap reference | Pod configuration event |
| S10 | Liveness probe failure | Restart and probe evidence |
| S11 | Named container port mismatch | Readiness and port evidence |
| S12 | Service target port mismatch | Service probe evidence |
| S13 | Invalid environment value | Application startup state |
| S14 | Missing Secret reference | Configuration reference error |
| S15 | Invalid working directory | Container startup path error |
| S16 | Missing configuration volume mount | Container mount state |
| S17 | Unsatisfiable node selector | Pending pod and scheduling event |
| S18 | Unsatisfiable node affinity | Pending pod and scheduling event |
| S19 | Zero replicas | Deployment replica state |
| S20 | Invalid startup arguments | Container start evidence |

The validation record reports alerting and investigation across S01–S20, with MCP evidence and RAG retrieval. Detailed remediation preparation, approvals, writes, and recovery outcomes have only been demonstrated for selected workflows; the complete live remediation matrix for all 20 scenarios is not claimed.
