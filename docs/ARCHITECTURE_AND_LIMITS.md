# Architecture, Model Use and Security Boundaries

This document explains the **existing** AIOA spArkHAT architecture relevant to the 2026 Meta AI hackathon. It separates model-generated advice from authorized host-side action.

## System path

```text
 User / Owner — Linux Mission Control or paired Android
            │
            ▼
 Native operator + signed HTTPS / Tailscale gateway
            │ identity, source/capsule, CSRF/PolicyKit and session checks
            ▼
 AIOA Core / MissionService / TransactionRunner
    ├─ SQLite operation, audit, outbox, receipt history
    ├─ Core warrants and governor — exact-cost owner decision
    ├─ Bounded GitHub READ — typed, signed observation
    └─ Meta provider — Muse Spark 1.3 (untrusted advisory text)
            │
            ▼
 Result + receipt + data hash + source/identity binding
            │
            ├─ Linux Chrome readback and Mission Control
            └─ Signed Android result / thread readback
```

### What happens during a valid model question?

1. An exact request ID and human-visible input are recorded before dispatch.
2. The owner separately approves **the exact operation and financial bound** in the existing local authority channel.
3. The Core validates identity, source, expiry, scope, risk and budget. No blanket approval from the model.
4. The Meta adapter invokes `muse-spark-1.3`, with a bounded request/response.
5. A signed and hashed receipt is stored. Android and Linux may read the same exact result.
6. If a dispatch acknowledgment is lost, the system reports UNKNOWN and reconciles by readback; it does **not** automatically repeat an uncertain paid or mutable effect.

### Meta use, clearly distinguished

- **Meta Model API:** actual live `muse-spark-1.3` reply has been verified in an earlier Android/Linux acceptance.
- **Muse Code / Codex:** engineering assistance was used during implementation. The coding CLI is **not itself proof** that AIOA Native executed autonomous mutations.
- **New candidate:** bounded signed GitHub READ context is available to Muse as **untrusted data**, not as an opportunity for prompts to grant themselves tools, credentials or WRITE privileges.

### Public capability boundaries

| Capability | Security contract | Product outcome |
|---|---|---|
| Repository facts | Fixed GitHub READ adapters, bounded results, signed receipt | Earlier live READ proven; new context UI acceptance pending |
| Financial authorization | PolicyKit / Core warrant / exact owner confirmation | Historical live accepted |
| Android status | TLS identity, signed nonce and expiry, saved trust | Earlier physical signed reconnect proven |
| Critical Prompt Loop | Five-stage 1+3+1 preview | No Native live model sequence in this release |
| GitHub mutation | Exact owner warrant + bounded executor + independent GitHub GET required | Not bound; blocked |
| Browser autonomy | Separate owner URL scope + true OS process/network egress confinement | Not live; blocked |
| Persistent semantic memory | Owner opt-in and provenance required | Native Save Knowledge off; not live |
| iOS | Independent native client needed | Not implemented |

## What judges can inspect

- [Main repository](https://github.com/luciferprosun/AIOA-spArkHAT)
- [Release candidate PR](https://github.com/luciferprosun/AIOA-spArkHAT/pull/41)
- [Source: Meta chat](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/runtime/meta_hackathon)
- [Source: Native GitHub read](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/runtime/mcp_bridge)
- [Source: Android](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/clients/android)
- [Test history](https://github.com/luciferprosun/AIOA-spArkHAT/actions)

No plain-text API keys, Keystore, private certificates, production SQLite journal, payment credentials or private pairing tokens should be present in a review package.

**Most important honesty test:** a proposed Python file or typed `issue.create` proposal is *not* a merged commit or proof of running an agent.
