<div align="center">

<img src="assets/icon.png" alt="Kingdom Recap" width="96" height="96">

# Kingdom Recap

Battle report analytics for Rise of Kingdoms. Runs offline on your own PC.

[![Latest release](https://img.shields.io/github/v/release/gregmal19/kingdom-recap-releases?label=latest)](../../releases/latest)
[![Downloads](https://img.shields.io/github/downloads/gregmal19/kingdom-recap-releases/total)](../../releases)
![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-0078D6)

**[Download the latest version](../../releases/latest)**

</div>

## Overview

Kingdom Recap reads the battle reports the game stores on your PC and turns them
into analytics the game does not provide:

- Battle analytics: PvP and PvE breakdowns, trade percentages, commander-pair results
- Resource tracking: gathering activity and resource flow over time
- Player statistics: performance across all of your accounts
- Kill points: earned versus conceded, per battle and per session
- Auto-scan: captures reports from the game's mail cache the moment they arrive,
  before the game deletes them
- Progress Companion: commander loadout planning and equipment tracking

## Installation

1. Download `KingdomRecap-Setup-<version>.exe` from the
   [latest release](../../releases/latest).
2. Run the installer. Windows SmartScreen may warn that the publisher is unknown,
   because the installer is not code-signed. Select "More info", then "Run anyway".
3. To verify a download, compare `Get-FileHash .\KingdomRecap-Setup-<version>.exe`
   in PowerShell against the release's `SHA256SUMS.txt`.

## First run

1. Enter your activation code. Builds are currently invite-only; activation
   requires an internet connection once, after which the app runs fully offline.
   Reinstalling on the same machine re-activates automatically.
2. Open Settings and set the Mail cache folder. It is inside the Rise of Kingdoms
   installation, typically
   `C:\Program Files (x86)\Rise of Kingdoms\Rise of Kingdoms Game\save\mailcache`.
3. Set the Decoded output folder to a folder of your choice. This becomes your
   permanent report archive: the game deletes a report from its cache once read,
   so this folder holds the only surviving copy.
4. Save, then run a Scan. Keep the app open while you play and reports are
   captured automatically.

## Requirements

- Windows 10 or 11, 64-bit
- Rise of Kingdoms installed on the same PC

## Frequently asked questions

**Is it safe to use with my account?**
The app only reads report files the game has already written to your own disk. It
never writes into the game's folders and makes no game-server requests.

**Does it upload my data?**
No. Battle data never leaves your machine; there are no accounts, no cloud
services, and no telemetry. The only network call is the one-time activation,
which sends your activation code and an anonymous machine identifier.

**Where do I get an activation code?**
Distribution is currently invite-only. Codes are issued with each invite and are
valid for one machine.

**Why does Windows warn me during installation?**
The installer is not code-signed. The warning concerns the missing signature, not
the contents of the app; the published checksum lets you verify the download.

## Version history

Every version and its notes are under [Releases](../../releases). A condensed
history is in [CHANGELOG.md](CHANGELOG.md).

## About this repository

This repository hosts downloads and documentation only. Kingdom Recap is free to
use; its source code is not public.
