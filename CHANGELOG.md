# Changelog

## Runtime 1.1.3 — 22 September 2026

- Adds explicit support for the captured Mimic Party v0.2.3 GameAssembly fingerprint.
- Keeps the shared Classic/Versus capacity helper patch fail-closed to known builds.
- Verifies the v0.2.3 helper retains the exact unique signature and stock 5/4 semantics despite moving in GameAssembly.dll.
- Keeps the live helper self-check that must return the configured capacity for mode selectors 0, 1 and 2.
- Revalidates the required v0.2.3 interop targets for max-player, playback voice-isolation and rematch hooks.
- Does not patch RoomListing values directly; the new room browser must reflect the room/session capacity rather than falsifying remote listings.
- Requires BepInEx Pack 1.0.1 for the v0.2.3 interop bootstrap.

## Packaging revision R3 — 11 September 2026

- Makes the main archive Expansion-only, with explicit Core and BepInEx Pack requirements.
- Connects all three Nexus pages and dedicated repositories.
- Places documentation in MimicParty10PlayerExpansion/ to prevent overwriting other guides.
- Keeps the verified Expansion 1.1.2 DLL byte-for-byte unchanged.

## Runtime 1.1.2

Corrects LaunchRematch(INetworkService) resolution, adds per-hook logging and preserves the shared Classic/Versus capacity helper with its live self-check.

## Legacy 1.0.x

Older on-disk distribution. Restore original game files before migrating.
