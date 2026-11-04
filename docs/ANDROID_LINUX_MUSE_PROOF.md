# Physical Android → Linux → Meta Muse Evidence

**Conclusion:** a real physical Android application completed an end-to-end Meta Model API **chat** with a preserved identity and a signed readback, on an earlier validated system. **Do not equate this with certification of the newest Linux release candidate or general autonomous agent operation.**

## The proven path

```text
Android AIOA Cosmic app
   │  request with device/session identity
   ▼
Private TLS 1.3 / Tailscale transport
   │  host certificate + pinned identity
   ▼
Linux Native Host — existing AIOA Core
   │  persisted proposal + exact human financial approval
   │  one-time warrant + governor
   ▼
Meta Model API → muse-spark-1.3
   │  one real request and one real response
   ▼
Core receipt / hashes / state SUCCEEDED
   ├── signed Android GET result + thread readback
   └── same conversation displayed in real Linux Chrome
```

### Verifiable historical request

| Field | Observed |
|---|---|
| Request ID | `89c750cf10f643798858a60de5fa7aaf` |
| Thread ID | `6b9e092798b7477ba6930c3bc116cbd6` |
| Provider | `meta_model_api` |
| Model | `muse-spark-1.3` |
| State | **SUCCEEDED** |
| Actor | **ANDROID** |
| Attempts / model calls | **1 / 1** |
| Reported usage | 229 prompt + 301 completion = 530 tokens |
| Usage estimate | USD 0.0015655 — **not an invoice** |
| Approved per-request ceiling | USD 0.05 (historical) |
| Response SHA-256 | `7f3bbcbb075fdcd54d5674bc400f4f548aa9d01fe1ca377a361c9ae48d2e0b27` |
| Signed Android result data SHA-256 | `aa2149c6b37be7f344e308e4ff514f660bb2ea03149f8d9cc0eccc8b1d2c3fe0` |
| Signed Android thread data SHA-256 | `a614dadddcc9b614341829c833e7a63ecfbda677edadd51456b9b5b725d5b24c` |
| Source of accepted demonstrator | `0b3f48ef0842833e17cf6bb79e8b72d44e7e7eee` |

The original response text was in Polish. We do not relabel it an English demonstration. This real request had an explicit owner financial decision and ended in a stored receipt. Other historical requests expired or remained UNKNOWN, and were not silently retried.

## Android artifact and signature

The known earlier app **4.1.0** was installed in place on a physical Xiaomi, preserving package identity, signer, Keystore and pairing records.

The later delivered but **not confirmed installed in the latest phase** APK has:

- Filename: `AIOA-Cosmic-4.1.1-debug-613737f.apk`
- Package: `eu.sparkhat.aioa.companion.cosmic4`
- versionCode: `402`
- Source SHA: `613737fc2b012594525e51664b24593f040e7a4a`
- Artifact SHA-256: `5e41aeeaa7c8128b83b2830e4c17b5374410fafdb5df25ba7250babd4e86c013`
- Signing certificate SHA-256: `3aa33eda63d3516010ddbf0fe0ff8de6b6dab6f6fc48088ee2592bde3b627bc4` (same signer family as the previously installed version).

The retained APK was rehashed in the local final release review, but **no new device install took place in that phase**.

### Independent checks and prior CI

- [Android build workflow — 82 tests, lint, assemble and signer validation](https://github.com/luciferprosun/AIOA-spArkHAT/actions/runs/41720343414)
- [Linux operator / Core acceptance workflow](https://github.com/luciferprosun/AIOA-spArkHAT/actions/runs/41756784319)
- [Main source: Android client](https://github.com/luciferprosun/AIOA-spArkHAT/tree/main/clients/android)

A different historical signed reconnect on source `b7f4002b2a945a52e8ae08b66fc6b4ceeb418f54` passed with the existing device key, saved pairing, matching host certificate pin and Core journal. That signed status proof was valid at capture time, **not forever**.

## Latest candidate: what remains to prove

For release candidate `a9b32797247883fbe4faadffad4262217465c53f`, the Android code/signing path was preserved, but a **fresh physical signed reconnect after the new Native release remains PENDING**. A known DNS/VPN connectivity blocker in an earlier Android session involved an inactive Tailscale VPN, not necessarily broken cryptography.

Recommended quick acceptance when owner and actual device are available:

1. Keep the same package, Keystore, pairing, host TLS identity and private state. Do **not** uninstall, clear data, reset trust or generate a new QR.
2. Confirm real VPN transport; open existing AIOA Cosmic, reconnect using saved trust, then perform one fresh signed **READ-only** status.
3. Compare device/session/scope/source/expiry and signed payload digest with Core's exact current journal.
4. Repeat after closing/reopening the app to verify recovery; label failure/unknown honestly.
5. Make **no new paid model call** solely to prove that status READ works.

The film may reasonably be Linux-first and cite this Android engineering proof. It must not imply a fresh 4.1.1 phone test occurred if it did not.

## Security and privacy

This report omits phone public key encodings, source-coupled session tokens, device unique identifiers, local bearer credentials, private pairing records, private journal contents and raw APK binaries. They are kept in authorized, local evidence archives, not this public documentation repository.
