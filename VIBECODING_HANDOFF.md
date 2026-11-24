<!-- VIBE-CURRENT-STATE:START -->
## Current repository facts (generated, authoritative only for the facts listed)

- Repository: `TheCuriousProcrastinator/Draftava-Updates`; local working branch: `main`.
- Version data below is read from the **Git index** (the files staged for commit).
- Source `appcast.xml`: version `1.4.12`, build `475`.
- GitHub publication: Published GitHub release `v1.4.12` (reported by GitHub API). Other distribution channels are **unverified**.
- This section does **not** establish local build success, manual QA, App Store/Chrome Web Store approval, notarization, live website deployment, or release-asset integrity.
- The narrative below maintains architecture, decisions, issues and test evidence. Its older status and version claims are **historical** unless explicitly reconciled with this section.
- Before executable changes, inspect the actual checkout and validate the **exact files** on the real Mac. No automatic GitHub Actions.

<!-- VIBE-CURRENT-STATE:END -->

# Draftava Updates - Development Handoff

## Current verified state - November 23, 2026

- Repository: TheCuriousProcrastinator/Draftava-Updates.
- Default branch: main.
- Latest published version: Draftava 1.4.10.
- Build: 473.
- Release tag: v1.4.10.
- Downloadable ZIP: Draftava-1.4.10.zip.
- Public assets include the release ZIP and release notes.
- Live Sparkle appcast announces 1.4.10 (473).
- Live appcast contains the expected download URL and EdDSA signature.
- The application release passed local signing, notarization and package checks.
- Published assets were verified by the Draftava release workflow.

## Responsibility

This repository hosts the Sparkle update feed and public release assets.
Application source is in TheCuriousProcrastinator/Draftava.

Do not modify application source or regenerate release ZIPs here.

## Update-feed URL

https://raw.githubusercontent.com/TheCuriousProcrastinator/Draftava-Updates/main/appcast.xml

## Publication workflow

- Build and validate executable changes in the actual local Draftava checkout.
- Sign, notarize, staple, package and verify the final release locally.
- Publish source and update GitHub releases using the verified artifact.
- Generate the signed Sparkle appcast from the final release ZIP.
- Verify live feed version, build, URL, signature and public ZIP.
- Record verified publication state in the handoff.
- No automatic GitHub Actions or unattended CI releases.

## Historical records

Complete earlier update-feed history remains available with:

git show a23682cc00f2cb10346f4a9b1bd420dce2aa78b6:VIBECODING_HANDOFF.md

## Next session

Verify the latest Draftava source release, both GitHub releases and live
appcast before publishing another update.
