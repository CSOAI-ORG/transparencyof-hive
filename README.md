# transparencyof.ai Hive 🐝

> Per-domain 7-layer autonomous Hive. Part of the MEOK 25-hive mesh
> (see [`meok-hive-architecture-2026-06-07`](https://github.com/CSOAI-ORG/meok-compliance-gateway/blob/chore/ci-hardening/FLEET_BASE.md)).

**Domain:** `transparencyof.ai`
**Tier:** `governance`
**Genesis:** 2026-06-07
**Status:** scaffolded — awaiting deployment

## The 7 layers

```
L7  PRESENTATION    clarity white + transparency sky (Open Design)
L6  ORCHESTRATION   Hermes sub-context (Kimi K2.6 / DeepSeek V3.5 / local)
L5  DOMAIN MCP      explainability-report-mcp, ai-bom-mcp, watermarking-authenticity-mcp
L4  AGENT MEMORY    agentmemory (v0.9.26) — shared mode
L3  KNOWLEDGE GRAPH Cognee subgraph — scope: model decisions, feature importances, decision paths, watermarks, BOM
L2  VERSIONED HIST  Memoria (v0.4.0) — namespace "transparencyof"
L1  DRIFT DETECTION mex — fail on score < 90
```

## Quickstart (one command, post-deploy)

```bash
git clone https://github.com/CSOAI-ORG/transparencyof-hive
cd transparencyof-hive
pip install -r requirements.txt
python spawn.py                  # EvoAgentX bootstrap
python -m mex check              # L1 drift detection
python -m server                 # L5 MCP server
```

## A2A Agent Card

This hive publishes its capabilities at
`https://transparencyof.ai/.well-known/agent-card.json` — see `agent-card.json`.

## Cross-hive calls

Per L6 (hermes.yml), this hive will only call MCPs from:
- its own tool list (`L5`)
- shared MEOK governance MCPs (csoai-governance-crosswalk-mcp, etc.)
- other hives via A2A with explicit user consent

## Revenue

£399-£1,499/mo. Most credible of the *of.ai cluster for actual build (DOMAINS.md).

## Related

- [MEOK Hive architecture](https://github.com/CSOAI-ORG/meok-compliance-gateway/blob/chore/ci-hardening/FLEET_BASE.md) — the genome
- [MEOK global strategy](meok-global-strategy-2026-06-07) — 7 global moves
- [Crown jewels](meok-crown-jewels-2026-06-07) — verified open-source stack
