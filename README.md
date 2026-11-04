# AIOA spArkHAT — Meta Global AI Developer Hackathon 2026

> **A builder's prayer:** May our evidence be stronger than our screenshots. May our failures remain visible, our authorizations explicit, and our small machine be measured by what it actually ran.

**Public jury dossier · Indie developer / technical build · 4 November 2026**

This repository is a **documentation companion**, NOT a second implementation or a substitute for source code.

## Start here

- **[Production source and commit history — AIOA spArkHAT](https://github.com/luciferprosun/AIOA-spArkHAT)** — the only canonical code repository.
- **[Current release candidate — PR #41](https://github.com/luciferprosun/AIOA-spArkHAT/pull/41)** — reviewed integration, checks and merge decision; verify live status on GitHub.
- **[Engineering prayer and sprint journal](PRAYER_AND_SPRINT_JOURNAL.md)** — the requested first-person reflection, deliberately separated from certification.
- **[Technical evidence](docs/TECHNICAL_EVIDENCE.md)** — what was tested and how to inspect it.
- **[Android → Linux → Muse proof](docs/ANDROID_LINUX_MUSE_PROOF.md)** — one historical, actual physical-phone Meta API success.
- **[Failure atlas](docs/FAILURE_ATLAS.md)** — incidents, fixes, open limitations.
- **[Release and submission status](docs/RELEASE_STATUS.md)** — what is ready and what is not.
- **[Architecture, security and capability boundaries](docs/ARCHITECTURE_AND_LIMITS.md)** — one Core, signed readbacks and human-controlled effects.
- **[Links and reviewer checklist](docs/JURY_ENTRY_POINTS.md)** — URLs we intend to give the judges.

## Why this project exists

AIOA spArkHAT is an AI-assisted operator system for Linux, with a companion Android app. A user can propose work to an AI model, while local policy, identity, budgets, receipts and an explicit owner decision determine what the system can actually do. For Meta's hackathon, we integrated **Muse Spark 1.3** through the Meta Model API into an existing governed Core, and exposed bounded GitHub read-only context through Linux Mission Control.

We developed the system on a **two-core, approximately 4 GiB RAM Linux Mint machine with about 4 GiB swap**. Instead of hiding resource pressure, difficult CI runs, lease expiry, and failed phone-to-host reconnects, we are publishing a factual engineering timeline.

## Evidence-led status — snapshot 4 November 2026

| Capability | Evidence level | Honest boundary |
|---|---|---|
| Core, transaction journal, human approval | **Implemented / historical live** | Current release candidate still requires deployment acceptance |
| Muse Spark 1.3 response over Meta API | **Historical real success** | One verified Android-origin request, not unlimited automation |
| Android ↔ Linux signed HTTPS/status | **Historical physical PASS** | Fresh reconnect on new release is pending |
| GitHub repository READ | **Historical real signed READ** | New candidate READ→Muse UI path still requires a fresh current-source proof |
| Linux White Hole Mission Control | **Candidate + isolated UI tests** | Final UI and launcher need live deployment and inspection |
| Critical Prompt Loop 1+3+1 | **Preview only** | Native live execution is not enabled |
| Memory / CockroachDB | **SQLite Core operational; adapters exist** | Native semantic memory/Cockroach deployment not qualified |
| GitHub WRITE, self-writing agent, live Chromium automation | **BLOCKED** | No verified owner-warranted live executor |
| Hackathon video and final submission | **PENDING** | This repository itself is not a submitted project |

**Do not read a green test as proof of a live effect.** Historical tests are labelled historical; isolated tests are not physical-device runs. A generated AI code proposal is not a commit.

## Verified evidence highlights

- An actual Android-origin Meta request, `89c750cf10f643798858a60de5fa7aaf`, succeeded with provider `meta_model_api`, model `muse-spark-1.3`, **one attempt and one model call**, 229 input + 301 output tokens. The Android signed readback and Linux Core observations matched; details in [Android proof](docs/ANDROID_LINUX_MUSE_PROOF.md).
- The Linux functional release candidate `a9b32797247883fbe4faadffad4262217465c53f` passed focused review: **61** chat/governance tests, **110** Core/Native/mobile tests, **8** source checks, **50** JavaScript tests, isolated browser geometry checks, and packaging. The *first* broad 2,765-test run failed (**13 FAIL, 1 ERROR**) and remains openly recorded; isolated re-runs of the 14 cases later passed.
- [Main code](https://github.com/luciferprosun/AIOA-spArkHAT) previously merged PR #40, and PR #41 contains the new candidate. At the time of drafting, **PR #41 was open**, so do not treat this candidate as already merged or deployed.

## We chose truth over a perfect frontend

The final look of Linux and Android may be less polished than planned. A polished mockup is not proof that an agent executed a write. The judges can inspect actual code, tests, architecture and documented failures rather than assume every envisioned feature shipped.

**Deadline:** 4 November 2026 at 21:00 Eastern Time, corresponding to **5 November 2026, 03:00 CET (Berlin)**. The official [event](https://cerebralvalley.ai/e/meta-ai-developer-hackathon) and the [submission form](https://cerebralvalley.ai/e/meta-ai-developer-hackathon/hackathon/submit) are separate from this repository.

## Evidence hygiene

No Meta API keys, private Android Keystore, host/TLS signing keys, bearer tokens, complete SQLite journals, session secrets, private host identifiers, or personally identifiable device records are included here. Internal evidence files live outside Git; public source and GitHub CI are the reproducible review surface.

**Status note:** this is an as-of snapshot, not a promise that a future run or an unsubmitted video exists.
