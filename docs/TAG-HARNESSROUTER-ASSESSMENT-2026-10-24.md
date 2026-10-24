# T.A.G. / GROKTRAPPER HarnessRouter assessment (draft)

Status: PROPOSED / NOT DEPLOYED. Date: 2026-10-24. Owner: NEURO. This document is a planning artifact, not proof of integration.

## Scope and boundaries
T.A.G. (Trappin' on Grok) is the public showcase collective; GROKTRAPPER is the laboratory; AGENTROPOLIS is the parent. Public demos must not disclose private architecture, proprietary source, secrets, or internal data. AGENTROPOLIS-NEURO-BUILDS is explicitly in the repository census and must not be omitted from future scope reviews; inclusion does not authorize code access or publication.

## Evidence status
- Grok Bot shared-computer and account-wide connector behavior: described in user-supplied third-party article; independently verify against current official documentation before relying on it.
- HarnessRouter: user-supplied screenshot describes a unified interface for Codex/Claude Code and OpenAI Responses compatibility. Backend isolation, Hermes support, auth model, provenance, version, and operational status are NOT VERIFIED.
- Hermes: existing AGENTROPOLIS orchestration candidate; actual adapter compatibility NOT VERIFIED.
- No credentials, connectors, schedules, agents, or infrastructure have been created by this assessment.

## Proposed execution contract
Intake (T.A.G. Grok Bot) -> scoped request -> AEGIS/54T external authorization -> broker -> optional HarnessRouter adapter -> approved Hermes/Codex/Claude executor -> immutable receipt -> independent VERITY review -> audit ledger.

HarnessRouter is an untrusted execution adapter, never a policy authority. Every task carries task_id, requesting identity, mandate, approved tool/action scope, data classification, expiry, approval reference, idempotency key, expected artifacts, and receipt destination. Reject missing, expired, broadened, or replayed grants. Enforce restrictions at the broker and executor, not only in prompts or model-based review.

## Compatibility matrix
| Component | Potential value | Verified here | Gate |
|---|---|---|---|
| Grok Bot | Intake, specialist collaboration | No, article only | Confirm session/connector sharing and approval controls |
| HarnessRouter | Unified harness dispatch | No, screenshot only | Verify upstream repo, license, versions, authentication, sandboxing, supply chain |
| Hermes | Inspectable orchestration | Existing project context only | Validate adapter/API and host isolation |
| Codex | Coding executor | Not tested | Scoped workspace and repository permission |
| Claude Code | Coding executor | Not tested | Scoped workspace and billing/access check |
| AEGIS / 54T | Authorization and containment | Proposed wiring | Independent deny-by-default enforcement |
| VERITY | Independent review | Proposed wiring | Evidence-backed pass/fail without self-approval |

## Initial specialist roster (proposal)
1. TAG-DISPATCH: accepts public-safe tasks; cannot execute or access secrets.
2. TAG-RESEARCH: source-based public research; no write permissions.
3. TAG-CREATOR: drafts accessible, neurodivergent-friendly content; never publishes autonomously.
4. TAG-QA: checks citations, outputs, privacy, and accessibility; cannot approve its own work.
5. TAG-HANDOFF: creates structured, scoped requests for a separate broker; cannot issue grants.

Keep bots few and narrow; never treat per-bot memory or profile separation as security isolation.

## Threat model
- Shared browser cookies and command-line credentials permit cross-bot lateral access.
- Prompt injection through webpages, repositories, tickets, or CSVs can request unsafe tool actions.
- Router or MCP adapter may amplify permissions or expose credentials.
- Tool-result spoofing and fabricated receipts may conceal failed or unauthorized execution.
- Untrusted code and dependency updates may compromise the execution host.

Controls: separate low-privilege identities; external short-lived scoped broker tokens; isolated execution environments; allowlisted tools; human approval for external writes, deployments, purchases, credential changes, and publishing; signed or independently stored receipts; no secrets in prompts or shared workspaces; default-deny local execution.

## Phased acceptance gates
0. Inventory existing TAG/GROKBOT/NEURO-BUILDS repos, ownership, and exposure. Read-only.
1. Verify HarnessRouter upstream URL, source/license, releases, advisories, supported backends, and security boundaries. No installation until reviewed.
2. Prototype mock task dispatch using synthetic support-ticket CSV, no real credentials or external writes.
3. Validate task_id correlation, denied action tests, injection resistance, cancellation, timeouts, receipt integrity, and independent VERITY review.
4. Human approval for any scoped live integration; promote only after documented evidence.

## Required first test
Given a synthetic support-ticket CSV, TAG-DISPATCH produces a bounded analysis request. TAG-RESEARCH returns a sanitized summary. TAG-CREATOR drafts a dashboard specification. TAG-QA verifies figures and accessibility. Broker must reject an injected instruction to read secrets or write to GitHub. Save the artifacts and failure receipts; do not deploy.

## Outstanding decisions
- Confirm authoritative HarnessRouter repository and release.
- Confirm whether a Hermes adapter is available or must be written.
- Confirm public showcase repository destination and explicit scope before any outward-facing publication.
- Confirm who signs authorization grants and where audit receipts live.
