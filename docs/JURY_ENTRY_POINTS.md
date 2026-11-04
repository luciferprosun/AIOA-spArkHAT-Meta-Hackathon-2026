# Judges — Where to Review AIOA spArkHAT

This is a documentation companion to one canonical application repository. To avoid confusion, use these links in order:

## Primary / mandatory source code link

**[https://github.com/luciferprosun/AIOA-spArkHAT](https://github.com/luciferprosun/AIOA-spArkHAT)**

This is the actual open-source implementation, main branch, runtime and tests. If the hackathon form accepts only one GitHub link, **use this link**, not the companion dossier.

## Supplemental engineering dossier

**[https://github.com/luciferprosun/AIOA-spArkHAT-Meta-Hackathon-2026](https://github.com/luciferprosun/AIOA-spArkHAT-Meta-Hackathon-2026)**

This is a public, text-first explanation for reviewers:
- [A builder's prayer — personal sprint story](../PRAYER_AND_SPRINT_JOURNAL.md)
- [Technical tests / verified vs. unverified](TECHNICAL_EVIDENCE.md)
- [Physical Android → Linux → Meta Muse evidence](ANDROID_LINUX_MUSE_PROOF.md)
- [Technical incidents and why things failed](FAILURE_ATLAS.md)
- [Current sprint and release constraints](RELEASE_STATUS.md)
- [Architecture / security boundaries](ARCHITECTURE_AND_LIMITS.md)

## Exact code review destinations

- [PR #40: merged integration](https://github.com/luciferprosun/AIOA-spArkHAT/pull/40)
- [PR #41: most recent candidate, see live state](https://github.com/luciferprosun/AIOA-spArkHAT/pull/41)
- [GitHub Actions and test logs](https://github.com/luciferprosun/AIOA-spArkHAT/actions)
- [Android source](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/clients/android)
- [Linux runtime and Meta integration](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/runtime)
- [Linux web interface](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/web)

## Reviewer introduction (copy-ready, English)

> AIOA spArkHAT is a human-governed AI operator system for Linux with a signed Android companion. During the Meta Global AI Developer Hackathon, we integrated Meta Muse Spark 1.3 with an existing Core that enforces exact human authorization, bounded model spending, signed readback and auditable operation receipts. A real Android-origin API call succeeded and returned a matching response on Android and Linux. We also verified bounded GitHub READ. Our public source documents the working components, while this jury dossier gives the evidence ledger, limitations, and an engineering failure atlas. Developed on a dual-core Linux machine with roughly 4 GiB RAM, the project prioritizes inspectable real behavior over a polished mockup. Features not yet live — including autonomous GitHub WRITE, production Chromium automation and full CPL execution — are clearly marked.

## Submission information

- **Official organizer:** [Cerebral Valley + Meta event](https://cerebralvalley.ai/e/meta-ai-developer-hackathon)
- **Official form:** [Hackathon submission form](https://cerebralvalley.ai/e/meta-ai-developer-hackathon/hackathon/submit)
- **Cutoff:** 4 November 2026, 9:00 PM ET / 5 November, 03:00 CET (Berlin)
- **Demo video URL:** **PENDING** until real recording, upload and link verification.
- **Submission confirmation / receipt:** **PENDING** until the owner submits and verifies the portal response.

We cannot claim that creating this GitHub documentation repository submits the project to the event.

### Important distinction

The initial product includes pre-existing AIOA development history. The hackathon-specific work is the Meta Muse integration, Android/Linux evidence correlation, selected governed READ path and current Mission Control work. The source repository is the technical record; the dossier is the human-readable story.
