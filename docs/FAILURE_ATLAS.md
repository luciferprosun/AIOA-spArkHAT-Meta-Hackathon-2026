# Engineering Failure Atlas — Problems We Actually Met

*A transparent retrospective on building under severe hardware and deadline constraints, as of 4 November 2026.*

This is an **updated** Markdown version of the earlier *Engineering Failure Atlas*. Its original early-morning snapshot predates a later successful physical Android→Muse call and PR #40 merge. The original failures remain history; stale OPEN statuses have been corrected below.

## Failures, fixes and residual risk

| ID | Observed failure / constraint | Engineering response | Evidence state |
|---|---|---|---|
| F-01 | Android chat authorization expired before inference; first request ended `CHAT_APPROVAL_EXPIRED` | Kept request failed, no fake Meta reply or retry; later a separately approved Android request successfully called Muse | **Historical failure; later bounded LIVE PASS** |
| F-02 | An English chat request could remain `UNKNOWN`, and an old UNKNOWN could hide a new successful conversation | Explicit current-source thread selection, independent UI BUSY lanes and retained UNKNOWN; test the language policy and exact receipt | **Candidate isolated tests; current release LIVE pending** |
| F-03 | Android↔private-host DNS/VPN path intermittently failed | Diagnostic readback identified Tailscale VPN not fully connected; owner reconnect required, no TLS/pairing reset | **Historical PASS on earlier source; new-source physical check pending** |
| F-04 | Chrome `about:blank` appeared ready before authenticated panel loaded | Validate exact expected HTTPS origin, complete document and secure context before private bootstrap | **Targeted tests and prior Chrome acceptance PASS** |
| F-05 | A two-core, ~4 GiB RAM Linux machine saturated its 4 GiB SWAP during Python/Chrome tests | Constrain parallelism; one code-writing integrator; bounded reviewers, isolate heavy tests | **Ongoing hardware constraint** |
| F-06 | Overlapping branches/worktrees and historical hackathon paths risked drift | Preserve one canonical code repo; PR #40 merged; freeze PR #41 candidate from verified existing integration | **PR #41 open as of snapshot; merge not presumed** |
| F-07 | First broad Python run: `2765` cases, **13 FAIL + 1 ERROR**, five allowed skips | Preserve failed logs, diagnose subprocess import/host environment; isolated reruns of all 14 offending cases PASS | **First run FAILED; focused rerun PASS, not full-suite PASS** |
| F-08 | Existing-profile launcher could open with missing host key/empty SQLite, or mutate before detecting occupied port 4317 | Fail-closed metadata/history checks; reserve target port before PolicyKit/Core; reject altered/missing trust state | **Candidate targeted tests PASS; deployment pending** |
| F-09 | Controller/Native shutdown could hang after an operator thread failed to start | Distinguish started/unstated handlers and close safely | **Candidate targeted tests PASS** |
| F-10 | A result receipt could become UNKNOWN for chat requests with approved budget above old USD 0.05 constraint | Align Linux owner policy and provider receipt accounting for configurable budget, preserve conservative risk and per-request approval | **Candidate targeted tests PASS; real deployment and billing gate pending** |
| F-11 | GitHub WRITE and Native worker existed as code contracts but not a production-qualified effect route | Keep disabled, propose typed advice only, demand source-bound owner warrants + verified executor before enabling | **Intentionally BLOCKED** |
| F-12 | Chromium browser research security is not achieved by URL string checks | Identified DNS rebinding, redirect, subresource, download/cookie, and OS egress containment gaps | **LIVE Chromium BLOCKED pending separate scope and network isolation** |

## Incident reproduction signatures

These strings may be found in public code/tests, private retained logs, or GitHub actions:

```text
CHAT_APPROVAL_EXPIRED
UNKNOWN
NATIVE_OPERATOR_DENIED_OR_UNKNOWN
EADDRINUSE / port 4317 occupied
CHROME_COMMAND_UNKNOWN
PAIRING_DNS_FAILED
test_lite_cli_constructs_nebius_route_from_host_injected_policies
```

**Interpretation matters.** A failed receipt due to owner approval expiry is not an outage of Meta's API. A browser transport timeout before page navigation is not proof that the UI lacks functionality. An environment-provided Nebius key can invalidate a test's precondition without implying that the current Meta provider is broken. In every case, reproduce and distinguish the source before changing code.

## Our stop rule

We do not turn off TLS, delete Core UNKNOWN, regenerate phone keys, overwrite the original journal, use a new fake local Core, or repeatedly pay for the same uncertain operation to make a demo appear successful. Regressions stay RED until investigated; an isolated retest is explicitly labelled as such.

## Scope and honesty

This atlas is a public account of engineering events, not a live monitoring dashboard. Review the latest [PR #41](https://github.com/luciferprosun/AIOA-spArkHAT/pull/41) and [GitHub Actions](https://github.com/luciferprosun/AIOA-spArkHAT/actions) for status changes. See [Technical Evidence](TECHNICAL_EVIDENCE.md) for test detail and [Android Proof](ANDROID_LINUX_MUSE_PROOF.md) for the actual Meta call.
