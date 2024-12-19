# WasabiGBA V0.2.4-SCFW

> [!NOTE]
> This is the baseline build of WasabiGBA that's guaranteed to work on GBA clones.
> Built successfully with the ff.:
> * [KS5360 build ee9413b](https://github.com/FluBBaOfWard/KS5360/tree/ee9413ba3b0563bb4172d43d5efe66f471382d9f)
> * [GBA Shared build b8d4fec](https://github.com/FluBBaOfWard/GBA_Shared/tree/b8d4fec9409cd8481431766a37abc45b500e0525)
> * [WasabiGBA build 1a844c2](https://github.com/OmDRetro/WasabiGBA-SCFW/commit/1a844c228567e254c6bc5cda3bcf46e1293334ec#diff-32e8fc5a7a6b9f84aa338b60ba373fe810b64cd87c9c8f4743b807e4bfb4ab28)
>
> This build also has _splash screen support_.


<img align="right" width="220" src="./logo.png" />

This is a Watara/QuickShot Supervision emulator for the Nintendo GBA.

## How to use

There is no builder included in the release yet.
The header is defined in Emubase.h, it's 64 bytes long, the size field is in
little endian, the 32bit id is 0x1A565357 (LE).
The name field can be 31 bytes plus a terminating zero.
There is an example header file included, "Supervision.header".

When the emulator starts, you press L+R to open up the menu.
Now you can use the cross to navigate the menus, A to select an option,
B to go back a step.

## Menu

### File

* Load Game: Select a game to load.
* Load State: Load a previously saved state of the currently running game.
* Save State: Save a state of the currently running game.
* Save Settings: Save the current settings.
* Reset Game: Reset the currently running game.

### Controller

* Autofire: Select if you want autofire.
* Swap A/B: Swap which GBA button is mapped to which SV button.

### Display

* Gamma: Lets you change the gamma ("brightness").
* Contrast: Change palette contrast.
* Palette: Here you can select between different palettes.

### Settings

* Speed: Switch between speed modes.
  * Normal: Game runs at it's normal speed.
  * 200%: Game runs at double speed.
  * Max: Games can run up to 4 times normal speed (might change).
  * 50%: Game runs at half speed.
* Sound: Turn on/off sound.
* Autoload State: Toggle Savestate autoloading. Automagically load the
 savestate associated with the selected game.
* Autosave Settings: This will save settings when leaving menu if any changes
 are made.
* Autopause Game: Toggle if the game should pause when opening the menu.
* Overclock EWRAM: Changes the waitstates on EWRAM between 2 and 1, might
 damage your GBA and uses more power, around 10% speedgain. Doesn't work on
 Gameboy Micro. Use at your own risk!
* Autosleep: Change the autosleep time, also see Sleep.

### Machine Settings

* Machine: Select the emulated machine.

### Debug

* Debug Output: Show an FPS meter for now.
* Step Frame: Emulate one frame.

### About

Some info about the emulator and game...

### Sleep

Put the GBA into sleepmode.
START+SELECT wakes up from sleep mode (activated from this menu or from	5/10/30	minutes of inactivity).

### Quit Emulator

Tries to reset the Flashcart and reboots the GBA.

## Controls

* GBA A & B buttons are mapped to Supervision A & B.
* GBA Start is mapped to Supervision Start.
* GBA Select is mapped to Supervision Select.
* GBA d-pad is mapped to Supervision d-pad.

## Games

All games should "work".

## Credits

Huge thanks to Loopy for the incredible PocketNES, without it this emu would
probably never have been made.
Thanks to:
	Peter Trauner & Kevin Horton for docs about the Supervision.
	Osman Celimli for docs, tests & help about the Supervision. <http://tailchao.com/Wataroo/>


Fredrik Ahlström

Twitter @TheRealFluBBa

<http://www.github.com/FluBBaOfWard>
