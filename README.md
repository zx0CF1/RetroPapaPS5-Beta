# Retro Papa PS5 Beta

Retro Papa is a native retro frontend for jailbroken PS5s. This repo contains beta builds.

No ROMs, disc images or PlayStation BIOS files are included.

## Install

### First install or update

1. Run your normal exploit / etaHEN setup.
2. Open PayloadManager.
3. Load `RetroPapa-Installer.elf`.
4. Wait for the Retro Papa notification.
5. Open Retro Papa from the Games screen.

### After a reboot

1. Run your normal exploit / etaHEN setup.
2. Open PayloadManager.
3. Load `RetroPapa-Start.elf`.
4. Open Retro Papa from Games.

You do not need to load the large installer after every reboot. `RetroPapa-Start.elf` only starts the resident Retro Papa service.

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

The beta package includes the current ROM folders, PS1 BIOS setup, controls and save instructions in `README.txt`.

## Existing data

The installer is meant to leave your own data alone, including ROMs, BIOS files, saves, states, settings and favorites. Keep a backup of anything important before testing beta builds anyway.

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
