# GCC High Security Readiness Checklist

**Target:** Microsoft 365 GCC High  
**Status:** Design only; none of these items has been validated in GCC High.

## Identity and access
- [ ] Verify eligible GCC High tenant and licensing.
- [ ] Configure Microsoft Entra Government identities and authentication.
- [ ] Require MFA and assess Conditional Access.
- [ ] Enforce least-privilege user/service permissions.
- [ ] Verify reviewer authorization and privileged access lifecycle.

## Data protection
- [ ] Identify applicable controlled-information requirements.
- [ ] Configure SharePoint permissions and external sharing restrictions.
- [ ] Validate sensitivity labels and independent classification enforcement.
- [ ] Assess applicable Microsoft Purview DLP capabilities.
- [ ] Specify retention and deletion.

## Power Platform
- [ ] Verify government-cloud service and connector support.
- [ ] Validate licenses, connector authentication, and data policies.
- [ ] Isolate development and production environments.
- [ ] Implement safe retries, errors, and reconciliation.

## Human approvals
- [ ] Verify reviewer identity and eligibility.
- [ ] Require explicit authorization before processing.
- [ ] Stop rejected workflows.
- [ ] Define timeouts, escalation, and decision logging.

## AI and third-party services
- [ ] Verify permitted service availability and endpoints.
- [ ] Obtain explicit authorization for data type and workload.
- [ ] Review processing, retention, and boundary protections.
- [ ] Prevent disallowed transfers and test protections.

## Audit and monitoring
- [ ] Define events, identifiers, decisions, and timestamps.
- [ ] Implement governed, access-controlled audit storage.
- [ ] Define retention, change protection, monitoring, and escalation.
- [ ] Exercise incident response and recovery.

**Deployment decision: NOT READY FOR PRODUCTION.**
