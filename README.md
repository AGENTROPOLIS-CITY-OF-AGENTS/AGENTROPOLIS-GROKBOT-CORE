# AGENTROPOLIS-GROKBOT-CORE (draft v0.1)

Shared DNA for every institutional GrokBot in Agentropolis. One core, many senior institutions, no zoo of unrelated prompts.
Status: DRAFT v0.1, published 2026-10-15 with NEURO approval. No agents created by this repo. Final authority: NEURO (human, Mission Control).

## Layers
1. **Intelligence Grid**: city OS (ASTRA, OMARCHY SCOUT, HERMES, AEGIS, APEX54, MEMORIA, DISPATCH, LEDGER, FORGE, ATLAS).
2. **District bots**: senior domain institutions (principal architect, CHAOS CODE, NTRU, SENTINEL-6, EXPLOIT WATCH, NEXUS PUBLICA, FISCALITH, ARC, MODEL LAB, EVALS, CREATOR, 789 STUDIOS, CHAOS RANK, BOTBAE, CONSTRUCTION, TERRA54, HOLOFOIL ARCANA54).
3. **Specialists**: these are temporary contexts (GrokBot subagents/modes) spawned by a senior bot. They are never permanent agents.

## Inheritance model
`schemas/grokbot-core.schema.json` defines 16 DNA fields. Each bot spec (`registry/wave1/*.yaml`) is an instance of it. Bots may extend but not drop or weaken fields. Permission tiers and evidence rules come from core and can only be tightened. The template is in `templates/SENIOR_AGENT_SYSTEM_SPEC.md`, and the full roster is `registry/registry.yaml`.

Mapping to real GrokBot platform primitives (from OptimusPrime twin v0, `/workspace/primer-twin/`):
| DNA field | Platform primitive |
|---|---|
| Identity / Mandate | agent profile (name, description, instructions) |
| Structured Memory | per-agent memory canon |
| Tool Manifest | connectors (MCP: Slack, GitHub, Origin, …) + native tools |
| Specialist Modes | executor subagents spawned per task |
| Eval / Regression | routines (scheduled) + skills |
| Receipts / Telemetry | files on shared box + LEDGER (future) |

Alignment with AGENTROPOLIS-ONTOLOGY: evidence uses `evidence-envelope-v1`, live bindings use `agent-entity-runtime-binding-v1`, and inter-bot coordination uses `district-agent-commons-v1` (communication_only, corridor Identity→Mandate→Policy→Tool Permission→Execution→Receipt→Audit). This repo references those schemas and does not redefine them.

## Loop
OBSERVE → CONTEXT LOAD → MODEL → DIAGNOSE → PLAN → RISK → AUTHORIZE → EXECUTE → TEST → VERIFY → RECORD → LEARN

## Doctrine
**Claimed ≠ Observed ≠ Installed ≠ Configured ≠ Reachable ≠ Running ≠ Authorized ≠ Verified.**
Every status claim carries one of these eight states and evidence. If a state has no evidence, the claim drops to CLAIMED.

## APEX54 provider boundary

APEX54 is AGENTROPOLIS-owned assurance identity and workflow. VERITY / Muse AI is a replaceable external development-time reviewer, not a required internal service or production authority. Existing implementation, identifiers, historical receipts and audit evidence must be preserved until separately migrated with compatibility tests. APEX54 does not authorize its own execution; AEGIS policy, scoped permissions and explicit human approval remain authoritative. This documentation correction does not establish production readiness.
