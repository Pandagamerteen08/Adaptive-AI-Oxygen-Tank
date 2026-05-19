# Model Guide

This guide explains how to create custom 3D models for Advanced Robotic Voice Oxygen Tank.

---

## Supported Runtime Format

Subnautica loads custom models using Unity AssetBundles.

Source formats such as FBX, OBJ, and BLEND must be imported into Unity and exported as AssetBundles.

---

## Required Prefab Name

Your AssetBundle must contain a prefab named:

```text
TankModel
```

---

## Recommended Specifications

* Under 10,000 triangles.
* Single material when possible.
* Proper UV mapping.
* Pivot centered.
* Realistic scale.

---

## Folder Location

```text
Assets/Models/adaptiveaioxygentank_model
```

---

## Unity Setup

1. Create a Unity project matching Subnautica's Unity version.
2. Import your model.
3. Create a prefab named `TankModel`.
4. Assign materials.
5. Build an AssetBundle.

---

## Troubleshooting

### Model Does Not Load

Check:

* AssetBundle filename.
* Prefab name.
* Shader compatibility.
* Correct config settings.

### Pink Materials

This usually indicates unsupported shaders. Use standard Unity shaders compatible with Subnautica.

---

## Best Practices

* Use efficient geometry.
* Minimize material count.
* Test in game.
* Include an inventory icon if needed.
