# 🔐 GenEscrow — Frontend Demo

Live demo site for **GenEscrow**, an AI-adjudicated escrow contract with sealed evidence binding on GenLayer (Bradbury).

- **Live demo:** https://hoveiser.github.io/genesrow-frontend/
- **Contract (v1.1.1):** `0x74300cc91f3E13e65822b919060f270d2bCE4194`
- **Explorer:** https://explorer-studio.genlayer.com/address/0x74300cc91f3E13e65822b919060f270d2bCE4194
- **Source code & full test matrix:** https://github.com/hoveiser/genesrow

## What this site shows

- Contract details with explorer links
- On-chain test results, each with verifiable transaction links:
  1. Happy path (client approve) — RELEASED
  2. AI approves (match) — RELEASED
  3. AI refunds (mismatch) — REFUNDED
  4. Retry + timeout refund (unreachable URL) — REFUNDED
  5. Appeal + final AI round — REFUNDED
  6. **Evidence mismatch (page mutated after delivery)** — REFUNDED

## Deployment history

| Version | Address | Purpose |
|---|---|---|
| **v1.1.1** (current) | `0x74300cc91f3E13e65822b919060f270d2bCE4194` | Sealed evidence binding + clean nondet closure |
| v1.1.0 | `0xAb243A38564BC2A3E3F738184b3A60E817A78337` | Evidence binding test suite |
| v1.0.0 | `0x020BEbbFA37b421F44Cc14ED485467969454f82D` | AI adjudication on visible text |
| v8.0 | `0xD4b28ce39A28fc5d4c43d9e85F1C4D3d6Eb5A815` | Safety mechanisms (timeouts, retry, appeal) |

## What changed in v1.1.x

**Sealed evidence binding:** the deliverable URL is fetched at delivery time, its visible text is hashed (sha256), and the hash is stored on-chain. At adjudication time, the URL is fetched again and the hash is verified before AI judges the content. If the page changed after delivery → `EVIDENCE_MISMATCH` verdict, automatic refund; live mutated content is never trusted.

Built for the GenLayer ecosystem — the adjudication layer for the agentic economy.
