# lucaspimentel's Scoop Bucket

[![Tests](https://github.com/lucaspimentel/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/lucaspimentel/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/lucaspimentel/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/lucaspimentel/scoop-bucket/actions/workflows/excavator.yml)

A [Scoop](https://scoop.sh) bucket for my CLI tools and PowerShell modules.

## Setup

```pwsh
scoop bucket add lucaspimentel https://github.com/lucaspimentel/scoop-bucket
```

## Apps

| App | Description |
|-----|-------------|
| [pscue](https://github.com/lucaspimentel/PSCue) | A PowerShell module that provides intelligent command-line completion and prediction. |
| [pwsh-prompt](https://github.com/lucaspimentel/pwsh-prompt) | A fast, minimal shell prompt for PowerShell, written in C#. |
| [cslint](https://github.com/lucaspimentel/cslint) | A fast C# linter that respects `.editorconfig`. |
| [wade](https://github.com/lucaspimentel/wade) | A terminal file browser with Miller columns, written in C#. |
| [analyze-assembly-size](https://github.com/lucaspimentel/analyze-assembly-size) | A command-line tool that analyzes the size of .NET assemblies, grouped by namespace. |

Pre-built binaries support Windows and Linux. macOS is supported when built from source.

## Install

```pwsh
scoop install lucaspimentel/<app-name>
```

## Post-install Notes

### pwsh-prompt

Add the following to your PowerShell profile to use pwsh-prompt:

```pwsh
function prompt { & pwsh-prompt }
```

### PSCue

After installing, import the module:

```pwsh
Import-Module PSCue
```
