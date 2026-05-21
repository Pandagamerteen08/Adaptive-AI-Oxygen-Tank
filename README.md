# Advanced Robotic Voice Oxygen Tank

A Subnautica BepInEx / Nautilus mod that adds a high-capacity AI-assisted oxygen tank with spoken alerts, configurable voice variants, emergency reserve behavior, custom audio packs, and optional custom models.

> **Note:** This project may expand beyond a single oxygen tank in future updates and evolve into a larger content mod.
>
> **Note:** A mod name change is planned for a future release.
>
> **Note:** I have **A LOT** Planned for this Subnautica Mod!

---

## Table of Contents

### Getting Started
* [Features](#features)
* [How to Install the Mod](#how-to-install-the-mod)
* [Compatibility](#compatibility)
* [File(s) you can Safely Remove Upon Download](#Files-you-can-safely-remove-upon-ownload)

### Versioning
* [Short Version](#short-version)
* [Long Version](#long-version)

### Features & Gameplay
* [Startup Boot Sequence](#startup-boot-sequence)
* [Personality Modes](#personality-modes)
* [Voice Presets](#voice-presets)
* [Audio Settings](#audio-settings)
* [Alert Types](#alert-types)
* [Emergency Oxygen Reserve](#emergency-oxygen-reserve)

### Crafting & Balance
* [Recipe](#recipe)

### Customization
* [Custom Voice Packs](#custom-voice-packs)
* [Required Voice Files](#required-voice-files)
* [Custom Model](#custom-model)
* [Model Guidelines](#model-guidelines)
* [Audio Layout](#audio-layout)

### Configuration & Setup
* [Installation](#installation)
* [Configuration](#configuration)
* [Configuration Reference](#configuration-reference)

### Performance & Compatibility
* [Performance Impact](#performance-impact)
* [Save Compatibility](#save-compatibility)

### Support & Documentation
* [Known Issues](#known-issues)
* [Known Limitations](#known-limitations)
* [Troubleshooting](#troubleshooting)
* [FAQ](#faq)

### Project Information
* [Roadmap](#roadmap)
* [Credits](#credits)
* [License](#license)
* [Additional Documentation](#additional-documentation)

---

## Features

* 475 O2 capacity.
* Unlocks from the Modification Station blueprint.
* Craftable at the Modification Station.
* Supports CustomCraft3 / Modification Station Mk2 as an optional dependency.
* Six built-in voice variants:

  * Robotic Male
  * Robotic Female
  * American Male
  * American Female
  * British Male
  * British Female
* Multiple personality modes.
* Preset system for saving configurations.
* OGG primary audio with matching WAV fallback and editing files.
* Packed audio archive loaded by the mod at runtime.
* Supplemental sound effects for warnings, startup, telemetry, and threats.
* Optional custom Unity AssetBundle tank model.
* Configurable voice, gender, personality mode, preset, volumes, and alert toggles.
* Emergency oxygen reserve that can activate once per full refill.
* Independent volume sliders for different audio categories.
* Support for custom voice packs.
* Safe to add or remove from existing saves.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## How to Install the Mod

1. Download the latest release.
2. Extract the downloaded `.zip` file.
3. Open the extracted folder.
4. Copy all contents into:

```text
Subnautica/BepInEx/plugins/AdaptiveAIOxygenTank/
```

Here is a video installation guide:

**Note:** That it may look a little bit different but the same will apply no matter what

[https://github.com/user-attachments/assets/0af8329c-092e-49c6-801d-1602caec446a](https://github.com/user-attachments/assets/0af8329c-092e-49c6-801d-1602caec446a)

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Compatibility

Supported:

* Subnautica (Tested on the Steam version only, but it will also most likly work on the Epic Games ver too!)
* BepInEx Pack for Subnautica
* Nautilus

Optional:

* CustomCraft3
* Modification Station Mk2

Tested on:

* Windows 10 (This mod has **NOT** been tested on Windows 10)
* Windows 11 (This mod has been tested on Windows 11)
* Steam version of Subnautica

> **Important:** This mod has only been tested on the Steam version of Subnautica.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

## Files you can Safely Remove Upon Download

**You can safely remove the Following file(s)**

.github/ISSUE_TEMPLATE

---

## How I Do My Updates

This project follows semantic versioning to clearly communicate the nature of each release.

### Short Version

🔢 **Version Format:** `vMAJOR.MINOR.PATCH[-TAG]`
- Example: `v1.2.0`, `v0.9.4-dev`, `v1.0.0-beta`

| Level | When Incremented | Examples |
|-------|-----------------|----------|
| **MAJOR** | Breaking changes, system overhauls, incompatible saves | Gameplay changes, core mechanic rewrites |
| **MINOR** | New features or content (backward compatible) | New voice packs, new personality modes |
| **PATCH** | Bug fixes, balance tweaks, performance improvements | Fixed crash, adjusted reserve amount |
| **TAG** | Pre-release versions (optional) | `-dev`, `-alpha`, `-beta`, `-rc` |


[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

### Long Version

🔢 **Version Format**
vMAJOR.MINOR.PATCH[-TAG]
Example: v1.2.0, v0.9.4-dev, v1.0.0-beta

---

🏗️ **MAJOR**
Incremented when changes fundamentally alter gameplay systems, core mechanics, save compatibility, APIs, or project structure.
A MAJOR increase indicates breaking changes and a clear separation from previous versions.
Backward compatibility is not guaranteed.

📦 **MINOR**
Incremented when new features, content, systems, or expansions are added without breaking existing functionality.
MINOR updates maintain compatibility with prior releases under the same MAJOR version.

🛠️ **PATCH**
Incremented for bug fixes, performance improvements, balance tweaks, and internal optimizations.
PATCH updates introduce no new features and do not alter expected behavior.

---

🏷️ **TAG (Optional State Identifier)**
Used only when a version is not considered a stable public release.

Allowed tags:

- `dev` → Active internal development build
- `alpha` → Early testing, incomplete systems
- `beta` → Feature-complete, testing for stability
- `rc` → Release candidate pending final approval

Tags are appended using a hyphen.
Example: v1.1.0-alpha

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Recipe

| Ingredient          | Quantity |
| ------------------- | -------: |
| Titanium Ingot      |        1 |
| Plasteel Ingot      |        1 |
| Lithium             |        2 |
| Silver Ore          |        2 |
| Gold                |        2 |
| Magnetite           |        2 |
| Computer Chip       |        1 |
| Advanced Wiring Kit |        2 |
| Power Cell          |        1 |

> **Note:** The crafting recipe is not final and may be adjusted for gameplay balance in future updates.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Startup Boot Sequence

When the tank is equipped, the onboard AI can play a customizable startup sequence.

Possible startup announcements include:

* Power initialization
* Oxygen sensor calibration
* Systems diagnostics
* Voice profile confirmation
* Capacity report

The startup sequence can be enabled, disabled, or replaced with custom audio.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Personality Modes

Personality modes change the wording, tone, and urgency of voice announcements.

Examples:

* Professional
* Friendly
* Scientific
* Military
* Calm
* Sarcastic

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Voice Presets

Presets store:

* Selected voice
* Personality mode
* Volume levels
* Enabled alerts
* Reserve settings

Users can create and switch between multiple saved presets.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Audio Settings

Separate volume controls are available for:

* Master volume
* Voice lines
* Startup sequence
* Warning alerts
* Threat alerts
* Ambient sound effects

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Alert Types

The tank can announce:

* Equip and unequip
* Oxygen percentage thresholds
* Rapid oxygen loss
* Entering dangerous biomes
* Predator proximity
* Low health
* Reserve activation
* Refill completion

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Emergency Oxygen Reserve

When the main oxygen supply is depleted, the tank can automatically activate a one-time emergency reserve.

Features:

* Activates once per full refill.
* Configurable reserve amount.
* Spoken activation announcement.
* Optional warning tones.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Audio Layout

Source audio is organized like this:

```text
Audio/VoiceLines/OGG/robotic_female/
Audio/VoiceLines/WAV/robotic_female/
```

Release builds do not include loose voice folders.

Audio is stored in:

```text
Audio/Audio.pak
```

This is a custom `AAO2PAK1` resource archive. The mod extracts it on first run, prefers OGG files, and falls back to WAV files.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Custom Voice Packs

Install voice packs under:

```text
Audio/CustomVoicePacks/PackName/
```

Each pack should include:

* `metadata.json`
* `OGG/`
* `WAV/`
* `preview.ogg`

Set the active pack in:

```text
config/AdaptiveAIOxygenTank.cfg
```

```ini
VoicePackSelection = PackName
```

### Example `metadata.json`

```json
{
  "name": "HAL 9000",
  "author": "ExampleUser",
  "version": "1.0.0",
  "description": "A calm and analytical voice pack.",
  "preview": "preview.ogg"
}
```

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Required Voice Files

Examples of commonly used voice lines:

* `startup.ogg`
* `oxygen_75.ogg`
* `oxygen_50.ogg`
* `oxygen_25.ogg`
* `oxygen_10.ogg`
* `oxygen_critical.ogg`
* `reserve_activated.ogg`
* `refill_complete.ogg`

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Custom Model

Recommended runtime format: Unity AssetBundle.

```text
Assets/Models/adaptiveaioxygentank_model
```

The AssetBundle should contain a prefab named:

```text
TankModel
```

FBX and OBJ are excellent source formats, but they must be converted into a Unity AssetBundle before Subnautica can load them.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Model Guidelines

Recommended:

* Under 10,000 triangles.
* Single material where possible.
* Pivot centered.
* Correct scale.
* Proper UV mapping.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Installation

Copy the contents of:

```text
bin/Release/AdaptiveAIOxygenTank/
```

into:

```text
Subnautica/BepInEx/plugins/AdaptiveAIOxygenTank/
```

Required:

* BepInEx Pack for Subnautica
* Nautilus

Optional:

* CustomCraft3
* Modification Station Mk2

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Configuration

Edit:

```text
Subnautica/BepInEx/plugins/AdaptiveAIOxygenTank/config/AdaptiveAIOxygenTank.cfg
```

Do not edit:

```text
config/com.bipnx.subnautica.adaptiveaioxygentank.cfg
```

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Configuration Reference

| Setting         | Description               |       Default |
| --------------- | ------------------------- | ------------: |
| TankCapacity    | Maximum oxygen capacity   |           475 |
| EnableVoice     | Enables spoken alerts     |          true |
| VoiceVariant    | Selected voice            | RoboticFemale |
| PersonalityMode | AI personality mode       |  Professional |
| EnableReserve   | Enables emergency reserve |          true |
| ReserveAmount   | Emergency reserve oxygen  |            75 |

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Performance Impact

The mod is designed to have minimal performance impact.

* Audio is loaded on demand.
* AssetBundles are cached.
* Voice packs are validated at startup.
* No measurable FPS impact under normal gameplay.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Save Compatibility

This mod is safe to add to or remove from existing saves.

If the mod is removed while the tank is equipped, the item may disappear from your inventory.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Known Issues

1. The oxygen tank may occasionally play voice lines at unexpected times.
2. The robotic voice may sometimes cut off before completing a full sentence.
3. Some non-robotic voice variants may not play correctly.
4. The mod may fail to read `AdaptiveAIOxygenTank.cfg`, causing the tank capacity to default to 520 O2 instead of the intended 475 O2.
5. The mod may not appear in FMU (Find My Updates Mod).
6. The mod may not appear in the in-game Mods menu, preventing configuration through the in-game interface.
7. The mod plays a sfx (Sound Effect) when load into the world

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Known Limitations

* Only one emergency reserve activation is available per full refill.
* Custom models must be packaged as Unity AssetBundles.
* Voice packs should include both OGG and WAV folders.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Troubleshooting

* If audio is missing, delete `Audio/.audiopak_extracted` and restart the game.
* If a custom model does not appear, verify the AssetBundle filename and prefab name.
* If a voice pack does not load, verify the folder name matches `VoicePackSelection`.
* If configuration changes do not apply, confirm you edited the correct config file.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## FAQ

### Can I use my own voice pack?

Yes. Create a custom voice pack and place it in `Audio/CustomVoicePacks/`.

### Can I disable spoken alerts?

Yes. Voice announcements can be disabled in the config file.

### Can I change the tank capacity?

Yes. The capacity can be modified in `AdaptiveAIOxygenTank.cfg`.

### Does this work with Subnautica: Below Zero?

No. At this time, only the original Subnautica is supported.

### Can I share my custom voice pack?

Yes. Voice packs are designed to be easily shared with other players.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Roadmap

Planned features:

* Additional voice variants.
* More personality modes.
* HUD indicators.
* Localization support.
* Expanded gameplay content beyond oxygen tanks.
* More Languages Check the Localization folder for the languages that will be added + more in the future
* Add another island with it's very own story line
* Pressing a button for a different dive mode
* A whole new story to the game

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Credits

* Unknown Worlds Entertainment for creating Subnautica.
* The BepInEx development team.
* The Nautilus development team.

See `Docs/Credits.md` for detailed credits.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## License

Released under the MIT License.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)

---

## Additional Documentation

The following additional guides are available in the `Docs/` directory:

### User Guides
* **[Docs/CHANGELOG.md](Docs/CHANGELOG.md)** - Complete version history and release notes
* **[Docs/VoicePackGuide.md](Docs/VoicePackGuide.md)** - Detailed guide for creating and installing custom voice packs
* **[Docs/ModelGuide.md](Docs/ModelGuide.md)** - Comprehensive guide for creating custom tank models
* **[Docs/ConfigurationReference.md](Docs/ConfigurationReference.md)** - Extended configuration options and advanced settings

### Project Documentation
* **[Docs/METADATA.md](Docs/METADATA.md)** - Project metadata and overview
* **[Docs/PROJECT_STRUCTURE.md](Docs/PROJECT_STRUCTURE.md)** - Directory and file organization

### Developer Documentation (Coming Soon)
* **CONTRIBUTING.md** - Guidelines for contributing to the project
* **ARCHITECTURE.md** - System design and architecture overview
* **API_REFERENCE.md** - Public API documentation

For more information, visit the **[Docs/README.md](Docs/README.md)** directory.

[⬆️ Back to Top](#advanced-robotic-voice-oxygen-tank)
