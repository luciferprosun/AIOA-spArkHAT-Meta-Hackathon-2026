# Technical Evidence and Review Index

**Evidence snapshot:** 4 November 2026. **Source of truth:** [AIOA spArkHAT](https://github.com/luciferprosun/AIOA-spArkHAT). This companion repository contains no runtime code and is not proof of a product feature by itself.

## 1. Live evidence (historical, bounded)

| Evidence | What it actually proves | Reference |
|---|---|---|
| Android-origin Meta API response | A physical phone requested Muse Spark 1.3; one exact owner-approved request succeeded; response and thread were signed and matched Linux Core. | [Android proof](ANDROID_LINUX_MUSE_PROOF.md) and public code |
| Native GitHub READ | One earlier fixed repository GET from Linux Core was signed, stored and independently compared to GitHub. | [Canonical source](https://github.com/luciferprosun/AIOA-spArkHAT) · [PR #40](https://github.com/luciferprosun/AIOA-spArkHAT/pull/40) |
| Human owner approval and UNKNOWN | A local PolicyKit / warrant / governor flow previously authorized a specific paid message; other uncertain requests remained unresolved, not retried. | [Android proof](ANDROID_LINUX_MUSE_PROOF.md) · runtime source |

The above successes occurred on **earlier deployed source versions**, not automatically on the new release candidate.

## 2. Current Linux release candidate

- **Candidate SHA:** `a9b32797247883fbe4faadffad4262217465c53f`.
- **Baseline main SHA before merge:** `23caa63619057b48c6b239ec0b5b946f1913e808`.
- **[PR #41 — governed Mission Control integration](https://github.com/luciferprosun/AIOA-spArkHAT/pull/41)**. Review the actual pull-request checks and merged state; never infer success from this static report.
- **Change summary:** one Core and state, private PolicyKit lease renewal, controlled Linux desktop launcher, independent UI polling lanes, signed GitHub READ as explicitly untrusted context for Meta Muse, ten navigation sections, bounded chat composer, preview-only CPL, honest memory status and configurable owner credit-policy gates.

**Targeted local result (not remote CI):**

| Test selection | Local result | Scope |
|---|---|---|
| Chat / money policy / Native lifecycle / provider | **61 PASS** | Owner review, financial accounting, response receipt |
| Core intent / tool / Native / mobile / HTTPS | **110 PASS** | Race, persistence, source checks, history and signed operations |
| Exact frozen-source / Android-contract / assets | **8 PASS** | Source identity and invariants |
| JavaScript | **50 PASS** | UI states, concurrency, display behavior |
| Contained Chrome | **PASS; 8 geometries** | **TEST_ONLY**, networkless / synthetic backend |
| Python AST/compilation | **24 changed files PASS** | Syntax/structural checks |
| Wheel + sdist | **PASS** | Packaging outside the source checkout |
| Python 3.11 Ruff (local) | **NOT_RUN** | Unavailable locally; CI is separate |

**Failed-first-run disclosure:** a prior broad `2765`-case run yielded **13 FAIL, 1 ERROR, 5 SKIP**, and was correctly recorded as FAILED. All 14 failure/error cases had a later isolated PASS, but this must not be presented as a full clean rerun of all 2765. See [Failure Atlas](FAILURE_ATLAS.md).

## 3. Reproducible review routes

- [Canonical main source](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main)
- [PR #41 source diff and live check status](https://github.com/luciferprosun/AIOA-spArkHAT/pull/41)
- [GitHub Actions for main repository](https://github.com/luciferprosun/AIOA-spArkHAT/actions)
- [Known earlier Android build workflow](https://github.com/luciferprosun/AIOA-spArkHAT/actions/runs/41720343414)
- [Known earlier Core CI](https://github.com/luciferprosun/AIOA-spArkHAT/actions/runs/41756784319)
- Source modules: `runtime/meta_hackathon/chat.py`, `runtime/meta_hackathon/native_tools.py`, `runtime/mcp_bridge/native_read.py`, `runtime/mission/warrant.py`, `runtime/memory_patch/persistence/ports.py`, `web/index.html`, `clients/android/`.

The private proof archive includes full JSON receipts, original APKs, device-side readbacks and screenshots, but is intentionally **not published** because it can contain privileged identity/session artifacts. Published hashes and source links supply narrower, independently inspectable evidence.

## 4. What this evidence DOES NOT prove

No verified Meta-controlled autonomous GitHub WRITE, no Native live worker, no full agent that edits code and commits, no approved real Chromium browsing with OS egress isolation, no live CockroachDB production data path, no iOS client, no ongoing 24/7 cloud operation. Later integration may change this, but each effect needs its own demonstrable receipt.
