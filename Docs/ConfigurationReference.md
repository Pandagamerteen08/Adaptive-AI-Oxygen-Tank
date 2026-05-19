# Configuration Reference

---

# Voice Pack Guide

This guide explains how to create custom voice packs for Advanced Robotic Voice Oxygen Tank.

---

## Folder Structure

```text
Audio/
└── CustomVoicePacks/
    └── MyVoicePack/
        ├── metadata.json
        ├── preview.ogg
        ├── OGG/
        │   ├── startup.ogg
        │   ├── oxygen_75.ogg
        │   └── ...
        └── WAV/
            ├── startup.wav
            ├── oxygen_75.wav
            └── ...
```

---

## metadata.json Example

```json
{
  "name": "My Voice Pack",
  "author": "Your Name",
  "version": "1.0.0",
  "description": "A custom voice pack.",
  "preview": "preview.ogg"
}
```

---

## Required Audio Files

Recommended files:

* startup
* oxygen_75
* oxygen_50
* oxygen_25
* oxygen_10
* oxygen_critical
* reserve_activated
* refill_complete
* equip
* unequip

Each file should exist in both OGG and WAV formats.

---

## Audio Specifications

Recommended:

* Mono or stereo
* 44.1 kHz
* 16-bit
* Normalized audio levels
* Minimal background noise

---

## Installing Your Voice Pack

1. Create your pack folder.
2. Add `metadata.json`.
3. Add audio files.
4. Set:

```ini
VoicePackSelection = MyVoicePack
```

in `AdaptiveAIOxygenTank.cfg`.

---

## Tips

* Keep file names lowercase.
* Use consistent volume levels.
* Test each line in game.
* Include a preview sample.

---

## Sharing

Compress your voice pack folder into a ZIP file and share it with other players.

---

## Version Compatibility

Ensure your voice pack is compatible with the current version of Advanced Robotic Voice Oxygen Tank. Include the compatible version numbers in your `metadata.json`:

```json
{
  "name": "My Voice Pack",
  "author": "Your Name",
  "version": "1.0.0",
  "description": "A custom voice pack.",
  "preview": "preview.ogg",
  "compatible_versions": ["1.0.0", "1.1.0"]
}
```

---

## Troubleshooting

### Voice pack not loading
- Verify the folder name matches the `VoicePackSelection` setting exactly (case-sensitive on Linux/Mac)
- Ensure `metadata.json` is properly formatted JSON
- Check that audio files exist in the specified directories

### Audio quality issues
- Verify audio specifications match the recommended settings
- Ensure audio files are not corrupted
- Test audio files with an external player

### Performance impact
- Large voice packs may impact load times
- Compress audio files appropriately
- Consider using lossy compression (OGG Vorbis) for smaller file sizes

---

## Technical Details

### File Format Support
- **OGG Vorbis**: Recommended for smaller file sizes and streaming
- **WAV**: Recommended for highest audio quality
- Both formats are supported simultaneously for flexibility

### Audio Processing
The game engine automatically selects the appropriate format based on system performance and user preferences. Providing both formats ensures optimal compatibility.

### Custom Metadata Fields
You can add optional custom fields to `metadata.json`:

```json
{
  "name": "My Voice Pack",
  "author": "Your Name",
  "version": "1.0.0",
  "description": "A custom voice pack.",
  "preview": "preview.ogg",
  "compatible_versions": ["1.0.0", "1.1.0"],
  "license": "CC-BY-SA 4.0",
  "website": "https://example.com",
  "support_email": "support@example.com"
}
```

---

# Configuration Reference

This document describes all configuration options available in `AdaptiveAIOxygenTank.cfg`.

---

## General Settings

| Setting               | Type | Default | Description                           |
| --------------------- | ---- | ------- | ------------------------------------- |
| TankCapacity          | int  | 475     | Maximum oxygen capacity.              |
| EnableVoice           | bool | true    | Enables spoken alerts.                |
| EnableStartupSequence | bool | true    | Plays startup audio when equipped.    |
| EnableReserve         | bool | true    | Enables emergency oxygen reserve.     |
| ReserveAmount         | int  | 75      | Oxygen granted by the reserve system. |

---

## Voice Settings

| Setting            | Type   | Default       | Description                    |
| ------------------ | ------ | ------------- | ------------------------------ |
| VoiceVariant       | string | RoboticFemale | Built-in voice to use.         |
| VoicePackSelection | string | Default       | Custom voice pack folder name. |
| PersonalityMode    | string | Professional  | Voice personality preset.      |

---

## Volume Settings

| Setting       | Type  | Default | Description                        |
| ------------- | ----- | ------- | ---------------------------------- |
| MasterVolume  | float | 1.0     | Overall volume multiplier.         |
| VoiceVolume   | float | 1.0     | Spoken voice line volume.          |
| StartupVolume | float | 1.0     | Startup sequence volume.           |
| WarningVolume | float | 1.0     | Warning tone volume.               |
| ThreatVolume  | float | 1.0     | Threat alert volume.               |
| EffectsVolume | float | 1.0     | Supplemental sound effects volume. |

---

## Alert Toggles

| Setting              | Type | Default | Description                    |
| -------------------- | ---- | ------- | ------------------------------ |
| AnnounceOxygenLevels | bool | true    | Announces oxygen thresholds.   |
| AnnouncePredators    | bool | true    | Announces nearby threats.      |
| AnnounceLowHealth    | bool | true    | Announces low health warnings. |
| AnnounceRefill       | bool | true    | Announces refill completion.   |

---

## Presets

Presets save:

* Voice variant
* Personality mode
* Volume levels
* Alert toggles
* Reserve settings

---

## Example Configuration

```ini
TankCapacity = 475
EnableVoice = true
VoiceVariant = RoboticFemale
PersonalityMode = Professional
EnableReserve = true
ReserveAmount = 75
MasterVolume = 1.0
```

---

## Configuration File Location

```text
Subnautica/BepInEx/plugins/AdaptiveAIOxygenTank/config/AdaptiveAIOxygenTank.cfg
```

---

## Important Note

Do not edit:

```text
config/com.bipnx.subnautica.adaptiveaioxygentank.cfg
```
