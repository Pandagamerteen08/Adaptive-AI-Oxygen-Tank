# 3D Models

Place your custom tank model bundle in this folder.

Recommended file to create:

```text
Assets/Models/adaptiveaioxygentank_model
```

Recommended prefab name inside the bundle:

```text
TankModel
```

## Supported Runtime Format

Subnautica uses Unity, so the only format that can be loaded at runtime
is a **Unity AssetBundle** (no file extension, or `.assets`).

### Recommended workflow

1. Model your tank in Blender (OBJ, FBX, or native `.blend`)
2. Import the mesh into **Unity 2019.4 LTS** (the version Subnautica uses)
3. Set up materials using Subnautica's shader (`MarmosetUBER`)
4. Export as an AssetBundle and drop the bundle file here
5. Name the bundle: `adaptiveaioxygentank_model`
6. Put a prefab named `TankModel` inside the bundle

The mod looks for this bundle automatically. You can change the bundle path
and prefab name in `config/AdaptiveAIOxygenTank.cfg`.

## Format Reference

| Format | Works at runtime? | Notes |
|--------|------------------|-------|
| Unity AssetBundle | ✅ Yes | Only viable option |
| OBJ | ❌ No | Import to Unity first |
| FBX | ❌ No | Import to Unity first |
| GLTF / GLB | ❌ No | Not natively supported |

## Poly Count Guideline

Subnautica equipment models are typically **500 – 2 000 triangles**.
Keep your model in that range for best performance.
