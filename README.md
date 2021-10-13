## **VoyagerNX**
A port of Star Trek Voyager: Elite Force Holomatch for the Nintendo Switch. Compatible with both controllers (including WIP gyroscope support!) and keyboard + mouse controls! Based off of Tulip Voyager (a fork of the Lilium Voyager ioquake3 engine). Currently all releases are built from the "main" branch.

![20211005_072659](https://user-images.githubusercontent.com/56975081/136713142-7ff13e8d-5202-4092-9974-55046e2dff2b.jpg)


## **Installation**
- Latest full build including game files can be downloaded and copied from <a href="https://accela.design/downloads/switch-homebrew/VoyagerNX.zip">here!<br/></a>
- Copy release files to /switch/ folder
- If providing your own baseoa files, copy baseEF from a copy of Holomatch, making sure not to replace any files.
- Launch via HBMenu (by pressing R, not album!)
- Set phasers to frag!

## **Bugs**
- Sleep mode causes the game and sometimes Horizon to crash. This seems to be common with ioquake3 ports and I have no idea what's causing this yet.
- Solo Match leads to a softlock at the end of every match. This can be worked around by using "Multi Match" to create a bot match instead. If you end up softlocked, you can close the game by pressing Down to open a terminal, pressing L to bring up a virtual keyboard, typing "/quit", pressing Return, then pressing Enter twice, which should get you back to HBMenu.
- A small amount of slowdown can happen during really hectic battles in larger maps. This mostly occurs in custom maps and happens regardless of graphical settings (although dropping the resolution may help).
- If you switch between controller and keyboard + mouse input mid-match, your camera may start spinning wildly. Just press ESC/+, click with your desired input, then press ESC/+ again and it should resolve it. This might not even be a real bug and might just be my wireless keyboard, but I'm putting it here just to be safe.

## **Controls**
- Left Trigger - Alt Attack
- Right Trigger - Attack
- Left Bumper - Crouch (or brings up keyboard when text fields are selected)
- Right Bumper - Jump
- X - Use
- Y - Taunt / Toggle Console (menu)
- A - Select
- D-Pad Left + Right - Weapon Select
- D-Pad Up - Zoom
- D-Pad Down - Toggle Console (in-game)
- Minus - Scores
- Plus - Menu
- Left Stick In - Vote No
- Right Stick In - Vote Yes

## Enable Gyro (EXPERIMENTAL)
Modify your hmconfig.cfg file to add these variables, or replace hmconfig.cfg with hmconfig_gyro.cfg:
```
seta in_gyromouse "1"
seta in_gyromouse_debug "0"
seta in_gyromouse_yaw_axis "0" // 0 for handheld, 1 for controller. Type the command in console without "seta" to swap between modes in-game.
seta in_gyromouse_pitch "-10"
seta in_gyromouse_yaw "-20.0"
seta in_gyromouse_pitch_ui "0.0"
seta in_gyromouse_yaw_ui "0.0"
```
## TODO

- Finish gyroscope support (75% of the way or so done, just need implement a way to call cvars depending on whether handheld or controller mode is detected + implement a menu item to enable/disable gyro settings).
- Possibly look into adding splitscreen?



[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate/?cmd=_s-xclick&hosted_button_id=8GF4A3XS7ZHFY)

## **Original ReadMe**
<img src="https://raw.githubusercontent.com/zturtleman/lilium-voyager/master/misc/lilium.png" width="64">

**Lilium Voyager** is a fork of **Lilium Voyager** is a fork of [ioquake3](https://github.com/ioquake/ioq3) for running _Star Trek Voyager: Elite Force Holomatch_ (multiplayer). It is based on Thilo Schulz' [ioEF engine](http://thilo.tjps.eu/efport-progress/) (also known as iostvoyHM). The focus for Lilium Voyager is to maintain Elite Force multiplayer support on newer ioquake3 versions.


Differences from ioEF 1.38-rc1 (2011):

  * Player origin rounding is compatible with the original QVMs (x86, x86_64).
  * Fixed "read past end of server message" error after downloading a pk3 using EF 1.2 protocol (24).
  * Network compatible with ioEF 1.37.
  * Dedicated servers are listed on official Raven master server.
  * Client and server use separate config files (from ioq3).
  * Better compatibility with newer operating systems (from ioq3).
  * VoIP uses Opus codec instead of Speex (from ioq3).
  * Support for ioquake3's OpenGL2 renderer.

Lilium Voyager code commits: [compare/upstream...master](https://github.com/zturtleman/lilium-voyager/compare/upstream...master)

The source code for the Elite Force game, cgame, and ui code is not included as it remains under a non-free license.

## Compiling

Lilium Voyager is compiled using `make`. For details see [building ioquake3](http://wiki.ioquake3.org/Building_ioquake3) and the [ioquake3 readme](README-ioq3.md).

For Nintendo Switch:

- Install and set up devkitA64.
- Ensure you have the latest versions of the following libraries installed in your dkA64 environment: libnx, switch-sdl2, switch-mesa, switch-libdrm_nouveau, switch-libjpeg-turbo, switch-zlib, switch-libogg, switch-libvorbis, switch-curl, switch-libmad (all covered by switch-portlibs: easy install: dkp-pacman -S switch-portlibs)
- Call make -f Makefile.nx in this directory. This will produce VoyagerNX.nro.
- Refer to the installation instructions on the releases to install and run the game on your Switch.

The Visual Studio project files are not supported.

Additional make variables not in ioquake3:
* `USE_CODEC_MP3=1` - Enable MP3 support using libmad (defaults to 1).
* `USE_INTERNAL_MP3=1` - Use libmad in the local source tree (defaults to 1).


## Discussion

  * [Discord (Fragmint★Wonderland)](https://discord.gg/7J2pjGD)


## License

Lilium Voyager is licensed under [the GNU GPLv2](COPYING.txt) (or at your option, any later version).


## Credits

* Quake 3 - id Software
* ioquake3 - ioquake3 contributors
* ioEF - Thilo Schulz & contributers
* Lilium Voyager - Zack Middleton
* Tulip Voyager - Daggolin


## Contributing

Please submit all patches as a GitHub pull request.
