# 10 Player Expansion for Mimic Party

**Runtime 1.1.4 · by arribbaa**

Up to **10 total players** in private Classic and Versus lobbies.

## v0.2.33

Runtime 1.1.4 adds the new captured v0.2.33 GameAssembly fingerprint. The shared Classic/Versus capacity helper still exists exactly once with the same verified stock 5/4 signature:

`33 C0 83 F9 01 0F 95 C0 83 C0 04 C3`

Current helper RVA: `0x1FCA310`.

Required reflected targets are still present for:
- FusionNetworkService.get_MaxPlayers
- OfflineNetworkService.get_MaxPlayers
- RoundController.SetPhase
- RoundController.PublishCurrentPlayer
- VoiceDirector.get_Open
- ResultsScreen.LaunchRematch
- ResultsScreen.DropSilentPlayers
- GameState.ResetForRematch

Requirements:
- BepInEx Pack 1.0.2
- Modding Core 1.0.0
