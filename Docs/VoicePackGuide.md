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
