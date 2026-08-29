# Retro Papa PS5 - Native Retro Frontend & Emulator Launcher (Jailbreak / etaHEN)

**Retro Papa** is a native retro gaming frontend and resident loader for jailbroken PlayStation 5 consoles. This repo contains beta builds..

No ROMs, disc images or PlayStation BIOS files are included.

## Install

### First install or manual update

1. Run your normal exploit / etaHEN setup.
2. Load `RetroPapa-Installer.elf` with PayloadManager or another PS5 ELF loader.
3. Wait for the Retro Papa notification.
4. Open Retro Papa from the Games screen.

From **v1.1.9b onward**, the installer also handles the resident service setup when PayloadManager is detected:

- installs/updates `retro-papa-native.elf` in PayloadManager's managed payload storage;
- adds `retro-papa-native.elf` to PayloadManager autoload if it is missing;
- preserves existing payload entries, delays and ordering;
- does **not** enable or disable PayloadManager autoload globally.

If PayloadManager is not installed, Retro Papa still installs normally.

### After a reboot - v1.1.9b and newer

If PayloadManager is installed **and its autoload feature is enabled**:

1. Run your normal exploit / etaHEN setup.
2. Start PayloadManager as usual.
3. Let its autoload sequence finish.
4. Wait for the `Retro Papa is ready` notification.
5. Open Retro Papa from Games.

`RetroPapa-Start.elf` is no longer required for the normal PayloadManager setup from v1.1.9b onward.

If PayloadManager is not installed, or if its autoload feature is disabled, start the installed resident with your usual PS5 ELF loader:

```text
/data/homebrew/RetroPapa/retro-papa-native.elf
```

Retro Papa does not force-enable PayloadManager autoload if you intentionally disabled it.

### Older beta builds

Betas before **v1.1.9b** used `RetroPapa-Start.elf` after a full reboot. Run the newer `RetroPapa-Installer.elf` once to migrate to the resident/autoload setup.

### In-app updates

From v1.1.9b onward, builds that have an OTA channel configured expose:

```text
Retro Papa -> Settings -> Update Retro Papa
```

OTA downloads are **DNS-independent**: once an OTA channel is configured, Retro Papa can download and install updates without requiring working DNS configuration on the PS5.

You can still install a newer beta manually with `RetroPapa-Installer.elf`.

## Tested on PS5

- Nintendo Entertainment System - Mednafen
- Super Nintendo - LakeSnes
- Mega Drive / Genesis - Mednafen
- PlayStation - Mednafen
- Arcade - FBNeo

## Not tested yet

Mednafen itself supports more systems, but they are not wired into Retro Papa or tested on PS5 yet:

- Apple II / II+ / IIe
- Atari Lynx
- Neo Geo Pocket / Color
- WonderSwan / WonderSwan Color
- Game Boy / Game Boy Color
- Game Boy Advance
- Virtual Boy
- PC Engine / TurboGrafx-16 / CD
- SuperGrafx
- PC-FX
- Sega Game Gear
- Sega Master System
- Sega Saturn

Do not treat these as supported yet. A system only moves to the tested list after it works through Retro Papa on real PS5 hardware.

The beta package includes the current ROM folder layout, PS1 BIOS setup, controls and save instructions in `README.txt`.

## Existing data

The installer is meant to leave your own data alone, including ROMs, BIOS files, saves, states, settings and favorites. Keep a backup of anything important before testing beta builds anyway.

When PayloadManager is present, Retro Papa only adds its own `retro-papa-native.elf` autoload entry if it is missing. Existing PayloadManager entries and delays are preserved.

## Downloads

Beta builds are posted in Releases. Each release includes hashes so you can verify the files you downloaded.

## Credits

Retro Papa uses or adapts work from these projects:

- ItsBlurf/BFplayer and ps5-payload-dev/websrv - resident launcher / ELF replacement core
- ps5-payload-dev/SDL - PS5 SDL2 port
- Mednafen 1.32.1 - NES, Mega Drive / Genesis and PlayStation emulation
- ps5-payload-dev/LakeSnes - Super Nintendo emulation
- ps5-payload-dev/FBNeo - Arcade emulation
- ps5-payload-dev/sdk and PacBrew - PS5 build toolchain and libraries
- nothings/stb - helper libraries
- Google Fonts Play - UI typeface
- OpenGameArt / todak-public CC0 tracks - menu music

Thanks to the original authors and maintainers of those projects.

## Bug reports

Please include:

- PS5 firmware
- exploit / etaHEN version
- Retro Papa build ID
- system and game tested
- what happened when launching
- whether L3 + R3 returned to Retro Papa
- save / auto-resume result, if relevant
- the exact error or bad behavior

Do not upload copyrighted ROMs or BIOS files with bug reports.
