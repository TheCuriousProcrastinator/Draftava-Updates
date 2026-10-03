# Draftava Updates - Development Handoff

**Updated:** 2026-10-02

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
