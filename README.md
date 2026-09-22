# 10 Player Expansion for Mimic Party

**Runtime 1.1.3 · by arribbaa**

Up to **10 total players** in Classic and Versus lobbies. Versus keeps the game's RED/BLUE selection: the mod does not impose equal teams or a separate five-player quota per side.

[Download on Nexus](https://www.nexusmods.com/mimicparty/mods/1) · [GitHub downloads](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/releases/latest) · [Report an issue](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/issues)

## Requirements

- [BepInEx Pack for Mimic Party](https://www.nexusmods.com/mimicparty/mods/3) **1.0.1**
- [Mimic Party Modding Core](https://www.nexusmods.com/mimicparty/mods/2) **1.0.0**
- Windows x64 / Steam / IL2CPP build listed in [Compatibility](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/blob/main/COMPATIBILITY.md)

The main ZIP contains the Expansion only. Install both requirements separately.

## Installation / update

1. Close Mimic Party.
2. Install/update BepInEx Pack 1.0.1 in the folder containing `Mimic Party.exe`.
3. Install Core 1.0.0 into the same folder.
4. Extract this Expansion ZIP there; it adds/replaces `BepInEx/plugins/MimicParty10PlayerExpansion.dll`.
5. Launch normally through Steam and allow interop generation to finish when required.

## Features and settings

Classic and Versus share the configured **total** capacity, default 10. After a successful start, close the game and edit:

`BepInEx/config/com.arribbaa.mimicparty.10playerexpansion.cfg`

```ini
[Multiplayer]
MaxPlayers = 10
```

Allowed range: **6–10**. Values outside it are clamped.

Runtime 1.1.3 explicitly recognizes both captured shared-capacity-helper builds. Mimic Party v0.2.3 moved the helper in GameAssembly.dll but retained the exact unique signature and stock behavior (Classic 5, Versus 4). The runtime patch remains signature-based and performs its live 10/10/10 helper self-check before declaring the Expansion active.

The Expansion also installs the existing playback voice-isolation and rematch keep-lobby hooks. v0.2.3 retains the required reflected targets. The new room-browser types are present in the build; public-room behavior is part of the live acceptance boundary rather than being rewritten blindly.

## Removal and troubleshooting

Close the game and remove only `BepInEx/plugins/MimicParty10PlayerExpansion.dll`. Keep Core/Pack if other mods use them. Native capacity changes are in memory and disappear when the process exits.

Unrecognized game version or loader failure: do not force the patch; check `BepInEx/LogOutput.log`.

[Compatibility](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/blob/main/COMPATIBILITY.md) · [Changelog](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/blob/main/CHANGELOG.md) · [Build instructions](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/blob/main/BUILDING.md) · [License](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/blob/main/LICENSE.txt) · [Security](https://github.com/LocoPablito/Mimic-Party-10-Player-Expansion/blob/main/SECURITY.md)
