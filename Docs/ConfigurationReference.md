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
