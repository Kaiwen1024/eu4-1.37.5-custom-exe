# EU4 1.37.5 Custom Executable

[中文说明](README.zh-CN.md)

This repository provides the current Windows x64 custom `eu4.exe` for
Europa Universalis IV 1.37.5.0 (Inca), built on November 9, 2026.
It is a combined executable build; its changes are not separate switches.

## Download

- [Download eu4.exe](https://raw.githubusercontent.com/Kaiwen1024/eu4-1.37.5-custom-exe/main/eu4.exe)
- [SHA256SUMS.txt](SHA256SUMS.txt)
- [Build details](release-manifest.json)
- [English Workshop description](WORKSHOP.en.txt)
- [Chinese Workshop description](WORKSHOP.zh-CN.txt)

## Included Changes

1. Ming-only remote diplomatic tributaries: relaxes the non-neighbor acceptance
   check when the initiating country tag is `MNG`. Other diplomatic eligibility
   conditions still apply.
2. Modded achievements: overrides the modified-game checksum eligibility flag.
   Other achievement requirements remain in effect.
3. Siege adjustment: changes the siege tactics-difference coefficient from
   `250` to `500`; this is not a universal siege-speed multiplier.
4. Ironman console: removes the Ironman input from the console-command
   restriction flag while retaining multiplayer restrictions.
5. Confucian holy-site side panel: moves the existing holy-site widgets for
   the companion Confucian mod. Other religions retain their original offsets.
   This includes the November 9 fix for the crash when opening the religion page.

The ASN.1 IA5STRING mapping is restored to its original value, `16`.
No game-speed or multithreading change is included.

## Installation

1. Close EU4.
2. In Steam, open EU4's installed files folder.
3. Back up the existing `eu4.exe` outside that folder.
4. Download this repository's `eu4.exe` and copy it into the game installation
   folder, replacing the executable there.
5. Enable the companion script mods in the Paradox Launcher as needed, then
   launch EU4.

This file is for EU4 **1.37.5.0 on Windows x64**. It does not include the game,
the Mandate mod, the custom tributary scripts, the Confucian expansion scripts,
or their Chinese localization. The Confucian panel requires the matching
companion mod for its GUI and religious content.

Subscribing to a Workshop mod does not perform this manual executable
replacement. A Steam game update or file-integrity check can restore the
original executable. Restore your backup to remove this executable patch.

## Verification

SHA-256:

```text
80A38EF0B4645F03DA1E789395723F77D7BCD67F294029FA70E385F4251FDDAD
```

Size: **39,422,464 bytes**.

The build passed static checks and 34 isolated cases that execute the game's
native position getter and setter. The same harness rejects the previous
crashing adapter. The repaired build has not yet received in-game confirmation;
these checks do not establish full game or save compatibility.

## Scope of the Companion Tributary Mod

The ordinary Force Tributary CB improvements apply to eligible Emperors of China
that possess that CB. The additional tributary interactions and the executable's
remote diplomatic tributary adjustment are specific to Ming (`MNG`).

The full bilingual Workshop descriptions are provided in the files linked above.
