# 🔐 GenEscrow — Frontend Demo

Live demo site for **GenEscrow**, an AI-adjudicated escrow contract with real payable custody on GenLayer (Bradbury).

- **Live demo:** https://hoveiser.github.io/genesrow-frontend/
- **Contract (v1.0.0):** `0x020BEbbFA37b421F44Cc14ED485467969454f82D`
- **Explorer:** https://explorer-studio.genlayer.com/address/0x020BEbbFA37b421F44Cc14ED485467969454f82D
- **Source code & full test matrix:** https://github.com/hoveiser/genesrow

## What this site shows

- Contract details with explorer links
- On-chain test results, each with verifiable transaction links:
  1. Happy path (client approve) — RELEASED
  2. AI approves (match) — RELEASED
  3. AI refunds (mismatch) — REFUNDED
  4. Retry + timeout refund (unreachable URL) — REFUNDED
  5. Appeal + final AI round — REFUNDED

## Deployment history

| Version | Address | Purpose |
|---|---|---|
| v1.0.0 (current) | `0x020BEbbFA37b421F44Cc14ED485467969454f82D` | Stable release, improved AI adjudication |
| v8.0 | `0xD4b28ce39A28fc5d4c43d9e85F1C4D3d6Eb5A815` | Safety mechanisms test suite |

## How it works

1. Client creates an escrow with agreed acceptance criteria and deposits GEN (payable)
2. Freelancer submits immutable evidence (`deliverable_url` + `evidence_hash`)
3. Client approves, or stays silent and `timeout_release` frees the funds
4. On dispute, AI validators fetch the deliverable's visible text and vote APPROVED / REFUNDED
5. Losing party may appeal once; the second AI round is final; `finalize` pays the winner

Built for the GenLayer ecosystem — the adjudication layer for the agentic economy.
