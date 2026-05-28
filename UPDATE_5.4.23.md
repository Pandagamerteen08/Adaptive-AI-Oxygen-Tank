# BepInEx 5.4.23-pack.3.1.1 Update

This document contains updates to support **BepInEx 5.4.23-pack.3.1.1**.

## Changes

### New Files Added

1. **`AdaptiveAIOxygenTank.csproj`**
   - .NET project file for building the plugin
   - Targets .NET Framework 4.6.2 (Subnautica compatible)
   - References BepInEx 5.4.23 core libraries
   - Includes Nautilus framework dependency

2. **`src/Plugin.cs`**
   - Main plugin class implementing `BaseUnityPlugin`
   - Proper BepInEx attribute declarations
   - Configuration system initialization
   - Logging setup for BepInEx 5.4.23

3. **`build.bat`**
   - Windows batch script for building the DLL
   - Automatic NuGet package restoration
   - Comprehensive error handling

4. **`build.sh`**
   - Bash script for Linux/macOS builds
   - Same functionality as `build.bat`

5. **`BUILDING.md`**
   - Detailed build instructions
   - Prerequisites and setup guide
   - Troubleshooting section

### Updated Files

- **`COMPATIBILITY.md`**: Updated with BepInEx 5.4.23-pack.3.1.1 version info

## Building Instructions

### Quick Build (Windows)
```bash
build.bat Release
```

### Quick Build (Linux/macOS)
```bash
chmod +x build.sh
./build.sh Release
```

### Manual Build (Any Platform)
```bash
dotnet build AdaptiveAIOxygenTank.csproj --configuration Release
```

### Git Bash (Windows)
```bash
dotnet build AdaptiveAIOxygenTank.csproj --configuration Release
```

## Output

DLL will be created at:
```
bin/Release/AdaptiveAIOxygenTank/AdaptiveAIOxygenTank.dll
```

## Deployment

Copy the entire `bin/Release/AdaptiveAIOxygenTank/` folder contents to:
```
Subnautica/BepInEx/plugins/AdaptiveAIOxygenTank/
```

## Requirements

- .NET SDK 6.0 or later
- BepInEx 5.4.23-pack.3.1.1 or compatible
- Nautilus framework 2.0.0+

## What's New in BepInEx 5.4.23-pack.3.1.1

- Unity 2022.3.62f3 compatibility fixes
- Doorstop v4.5.0 with improved injection
- Unity 6 logging fixes
- Long-term support (LTS) designation
- Enhanced compatibility with modern Unity versions

## API Compatibility

The plugin uses:
- **BepInEx.Core 5.4.23**: Core plugin framework
- **BepInEx.Settings 5.4.23**: Configuration management
- **Nautilus 2.0.0**: Subnautica modding framework

All APIs remain backward compatible with previous 5.4.x releases.

## Notes

- This is a minimal implementation focused on BepInEx 5.4.23 compatibility
- The main plugin logic (oxygen tank, voice system, etc.) should be added to `src/Plugin.cs`
- Configuration system is pre-configured and ready to use
- Post-build events copy config files automatically

## Next Steps

1. Review the build instructions in `BUILDING.md`
2. Update assembly paths in `AdaptiveAIOxygenTank.csproj`
3. Run the build script or manual build command
4. Deploy to Subnautica BepInEx plugins folder
5. Test with actual Subnautica installation

## Troubleshooting

See `BUILDING.md` for detailed troubleshooting guide.
