# EGOIST Client — Fabric 26.2

A client-side Minecraft Fabric utility and HUD mod, with a dark-violet draggable click GUI, module settings, keybinds and JSON config profiles.

## Target
- Minecraft: 26.2
- Java: 25
- Fabric Loader: 0.19.3
- Fabric API: 0.161.0+26.2
- Gradle: 9.5.1
- Fabric Loom: 1.17.13

## Implemented modules
- **Toggle Sprint**: client-side sprint helper, with a movement setting.
- **FPS Display**: enabled/disabled module with label, debug preference and position settings.
- **Coordinates**: coordinate overlay with facing/dimension preferences and position settings.

## GUI
- Right Shift opens/closes the EGOIST screen.
- Drag the top bar to move the panel.
- Category navigation on the left.
- Select modules and use the ON/OFF area to toggle.
- Select a module to expose up to three settings in the editor strip; boolean settings toggle and numeric settings increment/decrement by clicking either side of their value.
- The keybind row captures a key (Escape clears it); assigned keys toggle modules when pressed.
- Save/Load Profile controls persist the default profile.
- Violet accent animation and custom rendering.

## Config
Main config: `.minecraft/config/egoist.json`
Profile: `.minecraft/config/egoist-profiles/default.json`

Config includes module enable state, keybinds and setting values. Saves use a temporary file followed by a replace/move.

## Build
Requires Java 25 and Gradle 9.5.1:

```sh
gradle build
```

The GitHub Actions workflow installs Java 25 and Gradle 9.5.1 and uploads the built JAR.

## Verification status
Source and ZIP structure were inspected locally. Compilation and runtime testing remain pending because this environment does not have Java 25 or Gradle installed. Build in GitHub Actions to verify against the actual 26.2 mappings and dependencies.

This project intentionally does not include anti-cheat bypasses or multiplayer combat automation.
