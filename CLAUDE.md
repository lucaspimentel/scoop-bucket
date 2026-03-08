# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Scoop bucket for distributing lucaspimentel's CLI tools and PowerShell modules via the [Scoop](https://scoop.sh) package manager on Windows. Created from the [ScoopInstaller/BucketTemplate](https://github.com/ScoopInstaller/BucketTemplate).

## Repository Structure

- `bucket/` — Scoop app manifests (JSON). Each file defines one installable app.
- `bin/` — Helper scripts that wrap Scoop's built-in tools (require Scoop installed locally).
- `.github/workflows/` — CI (manifest validation via Pester tests) and Excavator (auto-update PRs).
- `deprecated/` — Manifests for removed apps (empty by default).
- `scripts/` — Post-install/uninstall scripts referenced by manifests (empty by default).

## Common Commands

All `bin/` scripts require Scoop installed. Run from the repo root.

```pwsh
# Validate manifests (runs Pester tests via Scoop's test suite)
.\bin\test.ps1

# Check for new versions of all apps
.\bin\checkver.ps1

# Check for new versions and auto-update manifests
.\bin\checkver.ps1 -Update

# Verify hashes for all manifests
.\bin\checkhashes.ps1

# Format all manifest JSON files
.\bin\formatjson.ps1

# Create auto-update PRs (used by Excavator workflow)
.\bin\auto-pr.ps1
```

## Manifest Conventions

- **Released tools**: Use real version, hash from release assets, and `checkver`/`autoupdate` for auto-updates.
- **Unreleased tools**: Use `"version": "0.0.0"` with empty hash `""` as placeholders.
- **Pre-release support**: `checkver` uses the `/releases` API endpoint (`$[0].tag_name`) instead of `/releases/latest`, since tools may only have pre-release tags.
- **Hash autoupdate**: All manifests extract hashes from a `checksums.txt` release asset via `"hash": { "url": "$baseurl/checksums.txt" }`.
- **Release artifact naming**: `{project}-{rid}.{ext}` (e.g., `pwsh-prompt-win-x64.zip`).
- **PowerShell modules**: Use `"psmodule"` key instead of `"bin"`.
