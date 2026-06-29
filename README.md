# FLQ Mod Registry

Remote registry for FLQ Launcher supported game mods.

The launcher should read `manifest.json`, match installed Steam games by `appid`, compare `version`, download DLL assets from the listed release URLs, and verify `sha256` before copying anything into a game folder.

## Current Mods

| Game | Steam App ID | Version | Target DLL |
| --- | --- | --- | --- |
| Bloons TD 6 | `960090` | `1.0.0` | `d3d11.dll` |
| The Binding of Isaac: Rebirth | `250900` | `1.0.0` | `opengl32.dll` |

## Update Rule

Bump the per-game `version` whenever the DLL changes. The launcher can treat a higher semantic version as an available update and use the SHA-256 hash to verify the downloaded DLL.
