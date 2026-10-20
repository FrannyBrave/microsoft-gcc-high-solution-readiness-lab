# NDS Secure Document Review — Operational Runbook

**Target:** Microsoft 365 GCC High  
**Status:** Proposed procedures, not validated in GCC High.

## Expected process
Authorized user submits document; verified classification and policies are checked; ineligible requests are logged and rejected; eligible requests enter authorized human review; approved requests proceed to authorized processing; rejected requests are logged and stopped.

## Daily monitoring
- Review failed, cancelled, pending, and unusually long-running workflows.
- Investigate repeated denials and abnormal patterns.
- Check approvals, connector authentication, and availability.
- Confirm audit delivery, alerting, and incident escalation.

## Troubleshooting

### Classification rejected
Review submitted and verified metadata, confirm configured policy, never override without authorization, and investigate unusual repetition.

### Approval not received
Check execution status, reviewer assignment and authorization, connector connection, approved notification channels, and timeout/escalation procedure.

### Human rejection
Validate recorded outcome, rejection audit execution, termination, and absence of downstream processing.

### Connector failure
Identify failed action, service state, credentials, connector approval, and potential boundary violations. Do not reroute information to unapproved systems.

### Duplicate or partial processing
Pause affected flow if authorized; correlate run and transaction IDs; reconcile downstream state; retry only through controlled recovery; document actions.

## Proposed production audit fields
Run ID, document reference (not contents), submitted and verified classification, requester identity, reviewer identity, approval ID, decision and timestamp, processing status, error and retry/termination reason. Protect records with access restrictions, retention, and monitoring.

## Escalation
Escalate suspected unauthorized controlled-data transfer, unauthorized reviewer, unapproved connector, missing audit events, or evidence that a rejected request continued.

## Change control
Document change; assess data flow and risks; validate permissions/connectors/policies; test positive, negative, and failure paths; get approvals; deploy with rollback; verify.

## Prototype limitations
Commercial prototype uses user-entered classifications, self-assigned approval, and Compose outputs in run history. It lacks independently enforced reviewer authorization, durable audit storage, timeout/retry policies, actual SharePoint/AI connectors, and all GCC High deployment testing.

**Readiness: NOT READY FOR PRODUCTION.**
