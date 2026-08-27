# CodexMeter Releases ◈

Public, checksum-verifiable release packages for **CodexMeter**, a local Codex token meter for macOS and Windows.

This repository contains release binaries, SHA-256 manifests, and the signed macOS Sparkle update feed. The application reads supported Codex session JSONL files locally; it does not require a Codex login, API key, browser cookie, telemetry, or cloud sync.

## Download

- [Latest macOS and Windows releases](https://github.com/HechoLP/CodexMeter-Releases/releases)
- macOS: Universal 2 DMG and ZIP for macOS 14 or later
- Windows: self-contained x64 and ARM64 portable ZIPs for Windows 10/11

Always download the matching checksum manifest from the same release and verify the package before running it.

## macOS certificate-free preview

The current macOS preview is ad-hoc signed and not notarized by Apple. After verifying the DMG against `SHA256SUMS.txt`, copy `CodexMeter.app` to `Applications`, then run:

```bash
xattr -dr com.apple.quarantine /Applications/CodexMeter.app
open /Applications/CodexMeter.app
```

The command removes macOS download quarantine for this app. Do not use it on a package from another source or when the checksum does not match.

## Windows portable preview

The Windows preview is not code-signed. Verify the ZIP against `SHA256SUMS-windows.txt`, extract it to a permanent folder, and run `CodexMeter.exe`. If Windows marks the verified executable as blocked:

```powershell
Unblock-File .\CodexMeter.exe
Start-Process .\CodexMeter.exe
```

## Automatic updates

macOS builds use the signed Sparkle feed published from the `update-feed` branch. Release archives are authenticated with an Ed25519 signature before extraction. Windows builds currently open this repository's Releases page when the user requests updates.

## Security

- Official packages are published only through this repository's Releases page.
- Verify SHA-256 manifests before first launch.
- Never download CodexMeter from an unofficial mirror.
- Report a suspected packaging or update issue through the source maintainer's private support channel.

CodexMeter is an unofficial utility and is not affiliated with or endorsed by OpenAI. Codex is a trademark of OpenAI.
