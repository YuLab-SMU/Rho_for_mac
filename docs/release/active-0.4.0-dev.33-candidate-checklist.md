# Rho 0.4.0-dev.33 Cross-Platform Candidate Checklist

Status: active replacement source contract; deterministic Provider-discovery
repair, file-lane test repair, AGPL LIC-1, and LIC-2 are protected-integrated;
SP-READY1 SignPath repository readiness, hosted validation, integration,
public policy deployment, private reporting, and default-branch rules pass;
PR #46 protected integration and EDITOR-VIEWPORT-R1 local implementation,
affected validation, and review pass; public-guidance deployment verification,
Issue #33 hosted integration, owner MFA audit, external application/GitHub App
configuration, exact candidate, installed acceptance, Windows signing, MAC5,
publication, and candidate updater evidence remain open

Date: 2026-08-11
Last updated: 2026-08-12

Change class: D1 correction of a nondeterministic test fixture and a bounded
editor-viewport defect plus the required D4 single-use replacement development
identity

Risk: R1 for test-only timeout-fixture and local editor-viewport behavior; R4
for hosted candidate, signing/notarization, Release, update site, or
publication action

Owning documents: CRED-UX3 owns the production Provider-discovery timeout,
bounds, redaction, and error classes. CRED-UX3-R1 owns only deterministic
verification of that existing behavior. WS2-R1-R1 and RENAME-RECOVERY-R1 retain
the installed editor-envelope correction carried forward from rejected
`dev.32`. The macOS arm64 specification owns packaging and trust gates. This
checklist alone owns the exact `0.4.0-dev.33` source identity and any future
candidate, installed, MAC5, publication, or updater evidence.

The active Issue #33 focus-stability specification owns
`EDITOR-VIEWPORT-R1`: background selection synchronization may not focus or
reveal the Monaco selection, while explicit navigation retains both
authorities. It changes no candidate workflow or release authority.

Authorization: after reviewing candidate run `31552396659`, its exact failure,
and the focused repair plan, the project owner explicitly instructed
`修复并推送` on 2026-08-11. This authorizes the bounded test-fixture repair,
synchronized replacement identity, complete affected validation, scoped
commit, upstream branch push, and Draft PR. It does not waive protected merge,
candidate, installed, Windows-signing, MAC5, publication, or updater gates.

After subsequently directing the next version to be merged and published, the
project owner instructed the agent to complete all remaining required work on
2026-08-12. That activates the bounded AGPL LIC-2 prerequisite: fixed
cross-platform license resources, About legal notice/reveal action, deterministic
contracts, and fail-closed macOS candidate resource verification. It authorizes
source implementation, validation, review, a scoped PR, and protected merge.
It does not authorize candidate construction before all source and Windows-
signing gates pass, and it does not waive installed, MAC5, publication, or
updater acceptance.

The owner's instruction to complete every remaining required item also
activates SP-READY1 under
`docs/plans/active-2026-08-11-signpath-application-readiness-spec.md`: remove
automatic update-network admission, add the truthful public policy and
ownership surfaces required before a SignPath application, validate them, and
stop at protected integration/external readiness. It does not authorize a
candidate or represent SignPath approval.

After reviewing the remaining Issue #33 reproduction, the project owner
explicitly instructed the agent to start the bounded viewport repair on
2026-08-12. This authorizes local source implementation, regression coverage,
complete affected validation, review, documentation reconciliation, and a
scoped commit. Protected push/integration and every candidate or publication
action remain separate gates.

`0.4.0-dev.32` is immutable and rejected. Its Windows artifact, source checks,
and failed macOS candidate result cannot be relabelled or composed into this
identity.

## Exact Identity

| Field | Required value | Current evidence |
| --- | --- | --- |
| Application version | `0.4.0-dev.33` | Cargo/lock, Tauri, npm/lock, frontend mock/cache, workflow defaults, release-contract tests, roadmap, checklist, and `NEWS.md` synchronized |
| `rho.bridge` version | `0.1.14` | unchanged; no exported R package contract changes |
| `rho.agent` version | `0.1.5` | unchanged; no exported R package contract changes |
| Store schema | `12` | unchanged; no persistence schema changes |
| Release tag/name | `v0.4.0-dev.33` / `Rho 0.4.0-dev.33` | reserved replacement identity only; no tag, artifact, or Release exists |
| Source repository | `YuLab-SMU/Rho` | authoritative integration target |
| Candidate source | future exact upstream default-branch commit after external signing readiness and production signing integration | upstream `main` `71dfd3a442a3a22abacd8a49e400ff8deae1760a` contains the integrated source repairs, AGPL LIC-1/LIC-2, SP-READY1, and PR #46; EDITOR-VIEWPORT-R1 remains a locally verified source amendment pending protected integration; no candidate exists |
| Windows/macOS artifacts | exact `dev.33` candidate only | not built |
| Release decision | source repair authorized; release `NO-GO` | every downstream artifact and acceptance gate remains open |

The identity is single-use. Any artifact-producing failed run or later
user-visible source change consumes it and requires another version.

## Repair Contract

- Production `reqwest` client construction, 15-second total timeout, one-
  request limit, no-redirect/no-retry policy, 1 MiB response bound, credential
  handling, redaction, and `timeout` error projection remain byte-for-byte
  unchanged.
- The regression server used for timeout verification must accept and record
  the request but never write a status line, headers, or body. A successful or
  empty discovery response is therefore not a competing test outcome.
- The test client retains an explicit short total timeout. The server retains
  a longer bounded read watchdog so a broken timeout cannot hang CI forever;
  watchdog closure must not be misreported as a timeout pass.
- The regression continues to prove the serialized response omits the injected
  credential. Existing oversized-body and adjacent discovery tests remain
  unchanged.
- No application UI, settings schema, Provider endpoint, model/routing state,
  credential source, network authority, persistence, project, execution, or
  release policy changes.

## Local Implementation And Verification Evidence

The test-only implementation extracts the existing bounded request reader and
adds a stalled server that records the request, writes no HTTP response, and
waits for client closure under a five-second read watchdog. The client uses an
explicit 250 ms total timeout. The response must classify as `timeout`, omit
the injected credential, and prove the expected `/v1/models` request reached
the server. Existing success, redirect, credential, oversized-body, parser,
endpoint, and settings-preservation tests remain unchanged.

Local source evidence passes:

- the exact regression once with visible output and 50 additional independent
  Cargo-process repetitions without any retry-after-failure;
- `cargo fmt --all -- --check`, locked all-target workspace check, and locked
  full workspace tests (desktop 176 passed plus one opt-in Keychain test
  ignored by design; server 59; store 108; every other executed suite passed);
- `node --check desktop/dist/app.js` and all 56 deterministic frontend/release
  contract scripts;
- complete `rho.bridge` and `rho.agent` local test suites;
- candidate-release and update-site dry runs plus the macOS Ark bootstrap
  failure fixtures; and
- `git diff --check`.

The deliberate post-test review hashed all `agent_llm.rs` source before its
`#[cfg(test)]` boundary in both upstream `main` and the worktree. Both hashes
are
`6ddba16e8794f76e30d1ec80d5a6df3ea043c1750dc2d635eb677e3c52316ee6`,
proving production Provider-discovery code is unchanged. Review also found no
new dependency, schema, credential, network, persistence, project, execution,
UI, or mutation authority and no blocking contract deviation.

EDITOR-VIEWPORT-R1 adds a caller-owned reveal intent at the existing Monaco
selection boundary. Its regression first failed on the unconditional
background reveal, then passed after the repair. JavaScript syntax, all 60
frontend contracts, locked Rust format/check and 365 workspace tests, both R
package suites with 695 combined expectations, and `git diff --check` pass.
Post-verification caller review found no explicit navigation path losing reveal
authority and no backend, mock-command, dependency, schema, persistence,
credential, project, execution, or filesystem change.

## Required Source Evidence

1. **PASS** — the focused timeout regression passes 51 consecutive local
   executions, including 50 independent Cargo processes.
2. **PASS** — the full `rho-desktop` target and locked Rust workspace pass
   without rerun-until-green normalization.
3. **PASS** — Rust format/check, all deterministic frontend/release contracts,
   both R package suites, and `git diff --check` pass.
4. **PASS** — separate post-test review proves production discovery source is
   byte-identical and finds no blocking deviation.
5. **PASS** — PR #43 exact head passed macOS/Windows stable and Rust 1.88.0 in
   run `31557415624` and merged as `3a3546bd76cc11761263a5af8e060ba73a4a0580`;
   AGPL PR #30 exact head passed the same four identities in run `31558086732`
   and merged as `f37276940499d80b4898f630d3c683e13a554a3f`.
6. **PASS** — LIC-2 exact head `bffc0a2ecbd6c05778e1b4d3de42c4b07dbd58f5`
   passed all four hosted identities in run `31560071505` and merged to
   upstream `main` as `39701241206df2e4492d1539e725500c6795c09e`.
7. **PASS** — SP-READY1 exact head
   `ee7100866d547c0a43ba814464a960e29846fa43` passed all four hosted
   identities in run `31561610111`, merged through PR #45 as
   `e6fec3ecc286db93aa38c227e896ef077bdf17bd`, and passed all four exact-main
   identities in run `31562213275`. Update-site run `31562817460`, private
   vulnerability reporting, and no-bypass default-branch ruleset `20728497`
   pass without creating a candidate or changing the published `dev.24`
   development manifest identity.
8. **SOURCE PASS / DEPLOYMENT OPEN** — PR #46 records the integrated evidence
   and closes two application-form conformance gaps with linked SignPath
   attribution plus an explicit pending-application disclosure, visible
   Windows/macOS uninstall instructions, and negative regression coverage. It
   protected-integrated as `71dfd3a442a3a22abacd8a49e400ff8deae1760a`;
   regenerated-site deployment and live verification remain open and cannot be
   preclaimed.
9. **LOCAL PASS / HOSTED OPEN** — EDITOR-VIEWPORT-R1 implementation, focused
   failing regression, all affected local validation, NEWS reconciliation, and
   post-verification review pass. Exact hosted-head validation and protected
   integration remain open; no candidate or installed acceptance is claimed.

Pre-merge update-site review found that making `license_boundary` globally
mandatory also rejected immutable published `0.4.0-dev.24` evidence and would
break regeneration of the live download page. LIC-2 therefore owns one narrow
compatibility correction: update-site ingestion may exempt only exact
`0.4.0-dev.24` macOS evidence from that newly introduced check. Candidate
construction, Draft publication admission, `dev.33`, and every unknown version
remain strict. Positive legacy regeneration plus `dev.33` and unknown-version
negative tests are required before the exact-head matrix is accepted.
The affected candidate/update-site sources and publication workflows must also
trigger that matrix, and stable jobs must execute the update-site self-test.

## Remaining Gates

1. **PASS** — implement, review, validate, and protected-integrate the bounded
   Provider and file-lane source repairs plus AGPL LIC-1.
2. **PASS** — implement and integrate SP-READY1, publish its policy links,
   enable private vulnerability reporting, and apply a no-bypass default-
   branch review ruleset.
3. **SOURCE PASS** — protected-integrate PR #46 as
   `71dfd3a442a3a22abacd8a49e400ff8deae1760a`; regenerate the public site
   and verify its linked policy and visible uninstall guidance.
4. Run exact-head hosted validation and protected-integrate the locally
   verified EDITOR-VIEWPORT-R1 source repair before constructing `dev.33`.
5. Obtain organization-owner MFA verification, submit and receive the SignPath
   Foundation decision, and install/configure the GitHub App without guessing
   organization, project, policy, or artifact-configuration identifiers.
6. Implement and validate the production two-stage executable/NSIS signing
   package with the real configuration and fail-closed negative/recovery paths.
7. After Windows-signing disposition, run one protected
   candidate workflow against the exact current upstream default-branch commit and
   independently verify Draft assets, hashes, identities, macOS trust evidence,
   and Draft-only state.
8. Perform exact installed `dev.33` References/Rename/editor-intelligence,
   Data Viewer, Issue #33, live-Provider repair, proposal Accept/verified Undo,
   startup, update, upgrade, uninstall, and Windows acceptance in proportion to
   the carried release risk.
9. Resolve Issue #26's Windows signing disposition without treating an
   unsigned installer as a public-release pass.
10. Prove the exact root `LICENSE` and `LICENSES.md` are bundled under the fixed
   Rho resource path, the About action reveals the installed license offline,
   and the installed bytes match the candidate source on both platforms.
11. Reconcile candidate evidence, then stop for explicit MAC5 GO. Publication
   and updater mutation remain separate actions.

## Current Decision

The original source repair, version synchronization, complete validation,
hosted matrices, AGPL LIC-1/LIC-2, and their protected integration pass.
SP-READY1 implementation, review, exact-head/main hosted validation,
integration, initial public policy deployment, private reporting, and default-
branch rules pass. PR #46 protected integration passes while its
public-guidance deployment verification remains open. EDITOR-VIEWPORT-R1 local
implementation, validation, review, and NEWS reconciliation pass; exact hosted
validation and protected integration remain open. Organization-owner MFA
review, SignPath approval/GitHub App configuration, production two-stage
Windows signing, and Issue #26's signing disposition remain open.
Current decision remains `NO-GO` for candidate construction. Exact candidate,
installed acceptance, acceptance upload, MAC5, public publication, and
candidate update-site mutation remain open.
