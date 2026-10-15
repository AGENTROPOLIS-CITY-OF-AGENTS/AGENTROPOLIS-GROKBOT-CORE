# AGENTROPOLIS-GROKBOT-CORE (local draft v0.1)

Shared DNA for every institutional GrokBot in Agentropolis. One core, many senior institutions, no zoo of unrelated prompts.
Status: LOCAL DRAFT. Not pushed, no agents created. Final authority: NEURO (human, Mission Control).

## Layers
1. **Intelligence Grid**: city OS (ASTRA, OMARCHY SCOUT, HERMES, AEGIS, VERITY, MEMORIA, DISPATCH, LEDGER, FORGE, ATLAS).
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
