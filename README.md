<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/dover-mark-dark.svg">
    <img src="assets/dover-mark-light.svg" alt="Dover" width="120">
  </picture>
</p>

<h1 align="center">scoop-dover</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Windows-amd64-0078D6?style=flat&logo=windows&logoColor=white" alt="Windows amd64">
</p>

<p align="center">
  Scoop bucket for <a href="https://www.usedover.app">Dover</a> on
  Windows — a local-first API client. Postman alternative that runs
  on your machine.
</p>

## Install

```powershell
scoop bucket add qoinly https://github.com/qoinly/scoop-dover
scoop install dover
```

## Update

```powershell
scoop update dover
```

## Uninstall

```powershell
scoop uninstall dover
```

## What's in this bucket

Just the manifest (`bucket/dover.json`) that points Scoop at the
release artifacts published as GitHub Releases on this repo. Source
for the Dover app itself lives in a private repo; binaries are free
to use.

## Builds

Each release ships the portable Windows executable:

- `Dover-<version>-windows-amd64.zip` — extracted to a single
  `Dover.exe`, ready to run.

Scoop installs the zip to `%USERPROFILE%\scoop\apps\dover\`,
registers a Start menu shortcut, and shims `Dover.exe` onto your
PATH. No admin rights required.

## Manual install (without Scoop)

Two paths if you'd rather not use Scoop:

1. **NSIS installer** — `Dover-Setup-<version>-windows-amd64.exe`
   from the [Releases page](https://github.com/qoinly/scoop-dover/releases).
   Registers in Add/Remove Programs, creates Start menu shortcut,
   ships an uninstaller. Requires admin to install.
2. **Portable zip** — `Dover-<version>-windows-amd64.zip` from the
   same Releases page. Unzip anywhere, double-click `Dover.exe`.

## Code signing

Builds are unsigned (no Authenticode certificate yet). Windows
SmartScreen will flag the first launch with a "Windows protected
your PC" prompt — click **More info** then **Run anyway**. This is
a known temporary workaround until the signing pipeline ships.

## Release notes

Each release's notes are attached to its GitHub Release page on the
upstream project:
<https://github.com/qoinly/homebrew-dover/releases>

(macOS and Windows artifacts ship in lockstep; the upstream brew
tap repo hosts the human-readable changelog.)

## Issues

Bug reports + feature requests for Dover itself go to the upstream
project's issue tracker (currently private). For bucket-specific
issues (manifest bugs, install failures), open an issue on this
repo.
