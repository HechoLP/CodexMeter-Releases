# CodexMeter Releases — Archived Compatibility

CodexMeter downloads, checksums, release notes, and the signed macOS update feed now live in the main [`HechoLP/CodexMeter`](https://github.com/HechoLP/CodexMeter) repository.

## Current release

- [Download CodexMeter 1.0.4 for macOS or Windows](https://github.com/HechoLP/CodexMeter/releases/tag/v1.0.4)
- [View all current releases](https://github.com/HechoLP/CodexMeter/releases)

Always download the matching checksum manifest from the same release and verify the package before running it.

## Why this repository remains public

macOS versions through 1.0.3 have this repository's `update-feed` URL embedded in the app. Its final signed feed points those installations to CodexMeter 1.0.4 in the main repository. After that update, the app reads the main repository's feed.

This repository is intentionally retained as a public, read-only compatibility endpoint. It must not be deleted or made private while an older installation may still need the bridge feed. No releases after the 1.0.4 migration notice are published here.

## Platform trust

CodexMeter packages are currently distributed without Apple Developer ID, Apple notarization, or a Microsoft publisher certificate. Verify the official SHA-256 manifest before bypassing Gatekeeper or SmartScreen. macOS update archives and the Sparkle appcast are separately authenticated with Ed25519 signatures.

CodexMeter is an unofficial utility and is not affiliated with or endorsed by OpenAI. Codex is a trademark of OpenAI.
