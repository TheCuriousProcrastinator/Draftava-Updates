# Draftava Updates - Development Handoff

**Updated:** 2026-10-02

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

## Current verified update-feed state

At this handoff:

- product: Draftava
- version: **1.3.5**
- build: **443**
- minimum macOS: **14.0**
- architecture requirement: **arm64**
- release asset: `Draftava-1.3.5.zip`
- release tag referenced by appcast: `v1.3.5`

The appcast enclosure points to the GitHub Release asset hosted in this repository.

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

Before the next Draftava release, verify this handoff against both the Draftava source repository and the current live update repository.
