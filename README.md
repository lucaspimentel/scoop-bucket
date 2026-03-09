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
| [pscue](https://github.com/lucaspimentel/PSCue) | A PowerShell module for managing terminal color themes with live preview. |
| [pwsh-prompt](https://github.com/lucaspimentel/pwsh-prompt) | A fast, minimal shell prompt for PowerShell. |
| [cslint](https://github.com/lucaspimentel/cslint) | A C# linting tool. |
| [wade](https://github.com/lucaspimentel/wade) | A CLI tool for searching and navigating directories. |
| [analyze-assembly-size](https://github.com/lucaspimentel/analyze-assembly-size) | A tool for analyzing .NET assembly sizes. |

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
