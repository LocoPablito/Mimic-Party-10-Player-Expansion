# Changelog

## Runtime 1.1.4 — 22 September 2026

- Adds explicit support for the captured Mimic Party v0.2.33 GameAssembly fingerprint.
- Confirms the shared Classic/Versus capacity helper remains unique with the same stock 5/4 signature.
- Records the current helper RVA `0x1FCA310`; runtime patch application begins at `0x1FCA315`.
- Keeps the shared-capacity path fail-closed to explicitly supported builds.
- Revalidates all required v0.2.33 interop targets for max-player, playback voice-isolation and rematch hooks.
- Keeps the live helper self-check that must return the configured capacity for mode selectors 0, 1 and 2.
- Live v0.2.33 acceptance passed: all hooks installed, native patch applied, 10/10/10 self-check passed, Classic/Versus mode cards displayed Up to 10, and the Classic private lobby displayed 1/10.
- Does not patch remote RoomListing values directly.
- Requires BepInEx Pack 1.0.2 for the v0.2.33 interop bootstrap.

## Runtime 1.1.3 — 22 September 2026

- Added explicit support for the captured Mimic Party v0.2.3 GameAssembly fingerprint.
- Kept the shared Classic/Versus capacity helper patch fail-closed to known builds.
- Revalidated the required v0.2.3 interop targets.

## Packaging revision R3 — 11 September 2026

- Made the main archive Expansion-only, with explicit Core and BepInEx Pack requirements.
- Connected all three Nexus pages and dedicated repositories.
- Placed documentation in MimicParty10PlayerExpansion/ to prevent overwriting other guides.
- Kept the verified Expansion 1.1.2 DLL byte-for-byte unchanged.

## Runtime 1.1.2

Corrected LaunchRematch(INetworkService) resolution, added per-hook logging and preserved the shared Classic/Versus capacity helper with its live self-check.

## Legacy 1.0.x

Older on-disk distribution. Restore original game files before migrating.
