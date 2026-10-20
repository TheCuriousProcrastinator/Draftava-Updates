<!-- VIBE-CURRENT-STATE:START -->
## Current repository facts (generated, authoritative only for the facts listed)

- Repository: `TheCuriousProcrastinator/Draftava-Updates`; local working branch: `main`.
- Version data below is read from the **Git index** (the files staged for commit).
- Source `appcast.xml`: version `1.3.12`, build `450`.
- GitHub publication: Published GitHub release `v1.3.12` (reported by GitHub API). Other distribution channels are **unverified**.
- This section does **not** establish local build success, manual QA, App Store/Chrome Web Store approval, notarization, live website deployment, or release-asset integrity.
- The narrative below maintains architecture, decisions, issues and test evidence. Its older status and version claims are **historical** unless explicitly reconciled with this section.
- Before executable changes, inspect the actual checkout and validate the **exact files** on the real Mac. No automatic GitHub Actions.

<!-- VIBE-CURRENT-STATE:END -->

# Draftava Updates - Development Handoff

## CURRENT VERIFIED UPDATE-FEED STATE — 2026-10-20 (READ FIRST)

- **Published release:** Draftava **v1.3.12, build 450**.
- **Application release source:** `52d186dd06b6c61db7ff06c8e70d9edb634ae4a6`.
- **Updates main before this documentation update:** `a51ab864343fa9d0e266c7cfa6585874c3a9595b`.
- **Source main before this documentation update:** `5404a4e1e4d41b69929f37423665e1f938300ee4`.
- **Release ZIP:** `Draftava-1.3.12.zip`, 5,268,519 bytes.
- **Verified ZIP SHA-256:** `c96096c7e2a395667ee21e343f363e145161ab65a64ca87d28fd3326355d3090`.
- **Sparkle appcast:** Version 1.3.12, build 450, macOS 14.0 minimum, arm64, correct download URL and EdDSA signature.
- **Verification:** Local Release build, signing checks, ZIP validation, both downloaded GitHub assets and live appcast verified.
- **Released changes:** Typing responsiveness, Obsidian window reuse and Idea drag/Undo cleanup.
- **Release state:** Already published. Do not republish v1.3.12.
- **Future work:** Use the validated local Mac release workflow; never run GitHub Actions automatically.
- **Precedence:** This section supersedes historical 2026-10-18 state below.


## Publish/release command - standing authorization (2026-10-13)

- When the user says "publish", "release", "make update", or equivalent, treat that statement as standing authorization to complete the full validated local release and publication workflow. Do not ask for additional publication consent or confirmation.
- Never create Terminal scripts that ask the user to type "PASS", "YES", or another validation or confirmation keyword before publishing. Never introduce case-sensitive validation gates. A user statement such as "pass", "passed", "works", or equivalent is an explicit confirmation of the corresponding manual tests, regardless of capitalization.
- If the exact source change has already passed required local build/tests and the user confirmed required manual verification, proceed immediately with committing the exact tested source, handoff update, release build/signing/packaging, GitHub releases, Sparkle appcast publication, and live verification. Do not ask the user to repeat validation.
- Keep the non-negotiable local validation gate: do not publish unvalidated executable/build-affecting changes. If required validation genuinely has not happened, stop and explain that blocker, with the minimum required local test instructions; do not pretend validation passed.
- Stop only for real blockers such as missing local validation, failed build/test, unsafe working tree, missing signing credentials, or a failed release step. Do not create arbitrary pauses, keyword prompts, or extra approvals. Do not run GitHub Actions automatically.
- If local Mac access is unavailable, supply one copy-pasteable, **noninteractive** Terminal block to carry out already-authorized release actions in the exact validated Mac checkout. Use existing credentials/keychain without inventing confirmation prompts. If genuine credentials or macOS prompts are unavoidable, report them as blockers, not additional publication-approval requests.
- This rule takes precedence over older handoff wording that might suggest an additional user confirmation after validation. It does not override mandatory validation or source-of-truth checks.


**Latest narrative state verified:** 2026-10-20 (earlier release history and policies remain documented below)

## Shared Vibe Coding workflow rules (2026-10-08)

### Documentation-only handoff exception
- When the user explicitly requests a documentation-only update, ChatGPT may edit the existing root `VIBECODING_HANDOFF.md` directly through GitHub without requiring a Mac build or a local checkout step.
- First inspect the actual repository, target branch, and existing handoff. Change only the handoff, preserve historical project context, and verify the resulting GitHub file and commit. Do not use this exception for application code, tests, scripts, configuration, workflows, version/build changes, release assets, or other build-affecting files.
- Before the next local development change, fetch the remote branch and reconcile the updated handoff with the local checkout. Never overwrite or silently reset unrelated local changes.
- The normal rule remains: validate the exact executable/build-affecting changes in the real Mac checkout before committing or pushing those changes. Include a current handoff with every meaningful validated development commit.

### Temporary worktrees, releases, and logs
- Create temporary Git worktrees under `/Users/alex/Desktop/tmp/<project>-...` using a project-specific name.
- Put release working folders, temporary release artifacts, staging directories, and build/release logs under `/Users/alex/Desktop/tmp/<project>-release-...`.
- Do not create disposable worktrees inside `/Users/alex/Documents/Vibe Coding`.
- Do not place release artifacts or logs directly on the Desktop root.
- After a successful verified release, remove temporary worktrees and temporary release artifacts when safe. Do not remove active worktrees, uncommitted work, published assets, or permanent project files.
- Retain failure logs only when useful for debugging; remove unnecessary temporary logs.
- These instructions govern future operations and take precedence over historical temporary-path examples elsewhere in this handoff.

### Low-overhead development defaults
- Use ChatGPT plus GitHub inspection and Mac-local Terminal scripts by default; do not use Codex, ChatGPT Work, separately billed API agents, or GitHub Actions runners unless explicitly requested.
- Prefer existing project scripts. Give one local command block to apply, build, test, and launch an executable change, then a separate commit/push block only after required validation is confirmed.
- Documentation-only updates under the exception above do not require a rebuild.

## Project

`Draftava-Updates` is the public Sparkle update-feed and release-asset repository for Draftava.

It is not the Draftava application source repository.

## Repository

- GitHub: `TheCuriousProcrastinator/Draftava-Updates`
- Default branch: `main`
- Source baseline before this policy migration: `fd1bf6f4d2e9334af31ea61402282b885e119178`
- Primary tracked file: `appcast.xml`

Always verify the current repository HEAD and live appcast before changing release metadata.

## Historical verified update-feed state — 2026-10-18 (superseded)

The current `main/appcast.xml` and GitHub Releases were checked against the published Draftava source:

- Product: **Draftava**.
- Current published release: **v1.3.11**, build **449** (published 2026-10-18).
- Application release source commit: `4742268442306ea3fe060b32dfe9a1d8d5005a99`. Draftava's `main` can advance via handoff-only commits after the tag; do not assume `main` equals tagged source.
- Latest verified `Draftava-Updates` `main` HEAD **before this documentation-only update**: `6b3bad5a73cf212bf5dcf52a9b931e4cbbf49151`; fetch the newly committed HEAD for subsequent work.
- Minimum macOS version advertised by Sparkle: **14.0**; hardware requirement: **arm64**.
- Release asset: `Draftava-1.3.11.zip`, **5,264,305 bytes**. Both Draftava source and updates GitHub Releases list this exact file and size.
- Sparkle appcast enclosure URL: `https://github.com/TheCuriousProcrastinator/Draftava-Updates/releases/download/v1.3.11/Draftava-1.3.11.zip`.
- The feed at `https://raw.githubusercontent.com/TheCuriousProcrastinator/Draftava-Updates/main/appcast.xml` contains version **1.3.11**, build **449**, and a nonempty Sparkle EdDSA signature. The source release handoff records local packaging/signature validation and matching downloaded ZIPs. Do not invent a new checksum or notarization result.
- The release includes UTF-8 rich-text paste and typing-sound performance fixes. Cross-Mac iCloud archived-conflict recovery testing remains outstanding; do not mistake shipping of non-destructive `Recover Archived Draft as Copy…` for full automatic restoration.
- **The former “current 1.3.8, build 446” statement was a 2026-10-13 historical snapshot and is superseded.** Next release work must use the inspected `main` source, actual latest release, and live appcast.
- This update changes the handoff only. The `appcast.xml`, releases, ZIP assets, tags, and update behavior are unchanged.

## Repository role

This repository is used for:

- Sparkle `appcast.xml`
- Draftava release tags
- downloadable Draftava release assets

The Draftava application source lives in:

`TheCuriousProcrastinator/Draftava`

Do not make application source changes here.

## GitHub Actions policy

There are currently **no GitHub Actions workflows** in this repository.

Keep it that way unless the user explicitly requests a manual clean-environment workflow.

No automatic GitHub Actions should be introduced for:

- pushes
- pull requests
- tags
- schedules
- release publication
- appcast updates

Draftava development, build, signing, notarization, packaging, and release validation are authoritative on the user's local Mac.

Publishing a Draftava release does not depend on GitHub Actions.

## Release workflow

For a Draftava release:

1. validate the application locally in the Draftava source checkout
2. build/sign/notarize/package locally as required
3. verify the final ZIP locally
4. commit and push validated Draftava source/release changes
5. create/push the release tag as applicable
6. publish the verified ZIP as a GitHub Release asset here
7. update `appcast.xml` with the exact final version/build, URL, length, and Sparkle signature
8. push the appcast update
9. verify the live GitHub Release asset and live appcast
10. confirm Sparkle can see the intended release when appropriate

Do not invent release metadata. Use values from the locally verified artifact.

## Important rule

A release-tag push must not automatically trigger GitHub Actions.

GitHub is release/update-feed hosting. Local Mac validation is authoritative.

## Policy migration scope

This migration adds only:

`VIBECODING_HANDOFF.md`

It does not change:

- `appcast.xml`
- any release
- any release asset
- any tag
- update behavior

## Next task

Before the next Draftava release, fetch and verify current `Draftava/main`, `Draftava-Updates/main`, the latest version/build, the actual tag and signed appcast. The 1.3.12 release is already published; do not re-publish it. Run all executable/build-affecting validation in the user's real Mac checkout before any source/release write. No GitHub Actions run is required.


## Automatic handoff synchronization (2026-10-19)

- The tracked `.githooks/pre-commit` runs `Tools/vibe_handoff.py sync-staged` locally. It reads version/build from the Git index, reads the GitHub published release, refreshes only the bounded generated current-state section and stages the handoff in the same commit. It does **not** modify application code or establish build/manual-test validation.
- On a fresh Mac checkout, run `sh .githooks/install.sh` once. It refuses to replace an existing pre-commit hook. Do not bypass hooks with `--no-verify`. Changes to feature behavior, debugging decisions, known issues, manual validation, and next work still require a human-maintained narrative entry after the exact local test passes.
- Do not commit or push any executable change before successful validation in the real Mac checkout. The tool makes documentation updates only; GitHub Actions remain manual only.
- Sparkle applications' release scripts refresh generated release facts in source and update-feed handoffs once their respective release milestones are reached. Verify the live release/feed before claiming publication succeeded. Projects without a scripted release must refresh and commit the handoff after externally verifying publication.
- If GitHub release status cannot be verified, or the handoff contains unstaged edits, the hook blocks rather than guessing or overwriting your changes.
