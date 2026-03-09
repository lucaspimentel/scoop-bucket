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
| [pscue](https://github.com/lucaspimentel/PSCue) | A PowerShell module for [TODO]. |
| [pwsh-prompt](https://github.com/lucaspimentel/pwsh-prompt) | A fast, minimal shell prompt for PowerShell, written in C#. |
| [cslint](https://github.com/lucaspimentel/cslint) | A C# linting tool that respects `.editorconfig`. |
| [wade](https://github.com/lucaspimentel/wade) | Another TUI file manager, written in C#. |
| [analyze-assembly-size](https://github.com/lucaspimentel/analyze-assembly-size) | Analyze the size of .NET assemblies. |

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
