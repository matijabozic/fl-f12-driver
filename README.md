# FL-F12 mechanical keyboard driver.

## What is this:
This is heavily modified driver for FL-F12 mechanical keyboard! While this keyboard is amazing 65% (68keys) keyboard, with 2.4Ghz and Bluetooth connectivity, it lacks good driver to edit FN layer. I modified existing driver and made it possible to change FN layer by editing `Cfg.ini`. 

## What's changed:

- Remapped [FN layer](http://www.keyboard-layout-editor.com/#/gists/fb33fbcd4c593b741d76de71936f6bbb) to better suite my needs
- Redesigned user interface
- Made this driver portable
- Changed it's service name to `FL-F12-Driver (32bit)`
- Lot's of little quality of life improvements

Only residue this driver leaves is `C:\Users\<username>\AppData\Local\FL-F12-driver` folder where it stores local keymaps, macros etc.

## How to use it:

Connect keyboard in USB mode and start `Driver.exe`.<br />

If you want to make changes to FN Layer:
- make sure driver application is closed
- edit `Cfg.ini` and setup Fn layer the way you want.
- start driver application and hit Restore.

You can factory reset keyboard by holding `FN + Esc` for ten seconds to restore settings from MCU.<br />
To apply settings you made in `Cfg.ini`, start the driver application and hit restore. This way settings are loaded from the driver application.

## Factory defined codes:

These are predefined codes you can use while editing `Cfg.ini`: 

- 0x0e000005 - Factory reset (10s)
- 0x0e000012 - Battery status
- 0x0e000001 - Lock WIN key

- 0x0e00000c - Bluetooth 1
- 0x0e00000d - Bluetooth 2
- 0x0e00000e - Bluetooth 3
- 0x0e000000 - 2.4Ghz (useless as 2.4Ghz keeps looking for connection continuously)

- 0x040000ea - Volume down
- 0x040000e9 - Volume up
- 0x040000E2 - Volume mute

- 0x0e000007 - RGB static mode
- 0x12000300 - RGB static color toggle
- 0x0b000300 - RGB dynamic mode / dynamic color toggle
- 0x0c000100 - RGB brightness up
- 0x0c000200 - RGB brightness down
- 0x0d000100 - RGB animation speed up
- 0x0d000200 - RGB animation speed down

- 0x0e000010 - Kills RGB ?!? Some power saving mode? Avoid for now!