# Compatibility

## Mimic Party v0.2.3 — captured 22 September 2026

- Windows x64 / Steam / IL2CPP
- Unity 6000.4.2f1
- BepInEx 6.0.0-be.788
- BepInEx Pack **1.0.1**
- Modding Core **1.0.0**
- Expansion **1.1.3**

GameAssembly.dll SHA-256:
`adc318d8ad108a2eac4e130421d20c21aef840d8ec44203fba667d6eef08e199`

Metadata SHA-256:
`96b52e058bbf5ea2a5218a2a6c01a9391c72eda9432b640bbdce8d2c10060405`

Static compatibility verification found exactly one copy of the shared capacity helper signature:

`33 C0 83 F9 01 0F 95 C0 83 C0 04 C3`

Its stock semantics remain Classic 5 / Versus 4. The helper moved in GameAssembly.dll, so Expansion 1.1.3 explicitly allowlists the new GameAssembly fingerprint instead of falling back to legacy native signatures.

The v0.2.3 generated interop assemblies retain the required hook targets, including `FusionNetworkService.get_MaxPlayers`, `RoundController.SetPhase`, `RoundController.PublishCurrentPlayer`, `VoiceDirector.get_Open`, `ResultsScreen.LaunchRematch`, `ResultsScreen.DropSilentPlayers` and `GameState.ResetForRematch`.

The update also contains the new room-browser/session-listing API (`RoomListing.PlayerCount`, `MaxPlayers`, `IsFull`, `CanJoin`). Expansion 1.1.3 does not falsify remote RoomListing data. Public-room display/join behavior remains a live acceptance check.

## Mimic Party v0.1.73 — captured 11 September 2026

GameAssembly.dll SHA-256:
`44bbc82bdae73c1c86559a1f091ee9c7a3ae510a02c2d83f16b686ecdd9c8b11`

Metadata SHA-256:
`1586b9dd69e488706671d35490cc16377a612ca3af521031ac44464929b21e94`

Expansion 1.1.2 and Core 1.0.0 loaded in the documented Windows session; the shared helper returned 10 for checked selectors and Classic displayed 1/10.

## Verification boundary

A complete ten-client match, every Versus team distribution and full large-group audio/rematch behavior are not implied by hook installation alone. Future game builds are not automatically supported.
