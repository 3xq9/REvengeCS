# REvengeCS

External cheat for Counter-Strike 2. Reads game memory and draws an overlay on
top of the game with a DirectX 11 + ImGui menu.

<p align="center">
  <a href="https://discord.gg/ZksZaUeDbW"><img src="https://img.shields.io/badge/Discord-join-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord" /></a>
</p>
## Features

- Aimbot
- ESP
- Visibility check
- Offset scanner
- ImGui menu with hotkeys

## Build

Needs Visual Studio 2022 (MSBuild, x64).

```
build.bat
```

Output: `x64\Release\REvengeCS.exe`. Run as admin with CS2 open.

## Offsets

`src/offsets.hpp` is generated with [cs2-dumper](https://github.com/a2x/cs2-dumper)
and is tied to a specific CS2 build. Regenerate it after a game update.

## Installer

`setup.iss` builds a Windows installer with Inno Setup.

## Layout

```
src/
  App.cpp            window + render loop
  D3DBackend.cpp     DirectX 11 overlay
  GameHack.cpp       feature logic
  Aimbot.cpp         aim
  VisibleCheck.cpp   visibility
  OffsetScanner.cpp  offset resolution
  Settings*.cpp      config + UI
  Hotkeys.cpp        keybinds
  imgui/             ImGui
```

## License

No resell, no rehost, no commercial use.
