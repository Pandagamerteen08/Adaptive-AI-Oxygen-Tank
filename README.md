# Advanced Robotic Voice Oxygen Tank

A Subnautica BepInEx / Nautilus mod that adds a high-capacity AI-assisted oxygen tank with spoken alerts, configurable voice variants, emergency reserve behavior, custom audio packs, and optional custom model support.

## How to Install the mod

1. unzip the downloaded file

2. Open the downloaded file and place all of the contents that is inside of the folder in the the folder that is named: AdaptiveAIOxygenTank inside of Subnautica\BepInEx\plugins

Here is a video that you can watch for a guide:

https://github.com/user-attachments/assets/0af8329c-092e-49c6-801d-1602caec446a

## Features

- 475 O2 capacity.
- Unlocks from the Modification Station blueprint.
- Craftable at the Modification Station.
- Supports CustomCraft3 / Modification Station Mk2 as an optional dependency.
- Six built-in voice variants: robotic male, robotic female, American male, American female, British male, British female.
- OGG primary audio with matching WAV fallback/editing files.
- Packed audio archive loaded by the mod at runtime.
- Supplemental sound effects for warnings, startup, telemetry, and threats.
- Optional custom Unity AssetBundle tank model.
- Configurable voice, gender, personality mode, preset, volumes, and alert toggles.
- Emergency oxygen reserve that can activate once per full refill.

## Recipe

| Ingredient | Quantity |
|---|---:|
| Titanium Ingot | 1 |
| Plasteel Ingot | 1 |
| Lithium | 2 |
| Silver Ore | 2 |
| Gold | 2 |
| Magnetite | 2 |
| Computer Chip | 1 |
| Advanced Wiring Kit | 2 |
| Power Cell | 1 |

## Audio Layout

Source audio is organized like this:

```text
Audio/VoiceLines/OGG/robotic_female/
Audio/VoiceLines/WAV/robotic_female/
```

Release builds do not include loose voice folders. Audio is stored in `Audio/Audio.pak`, a custom `AAO2PAK1` resource archive. The mod extracts it on first run, prefers OGG, and falls back to WAV.

## Custom Voice Packs

Install voice packs under:

```text
Audio/CustomVoicePacks/PackName/
```

Each pack should include `metadata.json`, matching `OGG` and `WAV` folders, and a preview sample. Set `VoicePackSelection = PackName` in `config/AdaptiveAIOxygenTank.cfg`.

## Custom Model

Recommended runtime format: Unity AssetBundle.

```text
Assets/Models/adaptiveaioxygentank_model
```

The bundle should contain a prefab named `TankModel`. FBX and OBJ are good source formats, but Subnautica cannot load them directly at runtime without converting them through Unity.

## Installation

Copy the contents of `bin/Release/AdaptiveAIOxygenTank/` into:

```text
Subnautica/BepInEx/plugins/AdaptiveAIOxygenTank/
```

Required:

- BepInEx Pack for Subnautica
- Nautilus

Optional:

- CustomCraft3 / Modification Station Mk2 support

## Configuration

Edit:

```text
config/AdaptiveAIOxygenTank.cfg
```

Do not edit:

```text
config/com.bipnx.subnautica.adaptiveaioxygentank.cfg
```

## Troubleshooting

- If audio is missing, delete `Audio/.audiopak_extracted` and restart the game so the pack extracts again.
- If a custom model does not appear, verify the AssetBundle filename and prefab name match the config.
- If a voice pack does not load, verify the folder name matches `VoicePackSelection`.

See `Docs/Credits.md` and `Docs/CHANGELOG.md` for release notes and credits.
