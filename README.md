## **VoyagerNX**
A port of Star Trek Voyager: Elite Force Holomatch for the Nintendo Switch. Compatible with both controllers (including gyroscope support!) and keyboard + mouse controls! Based off of Tulip Voyager (a fork of the Lilium Voyager ioquake3 engine). Currently all releases are built from the "main" branch.

![20211005_072659](https://user-images.githubusercontent.com/56975081/136713142-7ff13e8d-5202-4092-9974-55046e2dff2b.jpg)


## **Installation**
- Copy release files to /switch/ folder
- Copy baseEF from your copy of STV:EFH, making sure not to replace any files.
- Launch via HBMenu (by pressing R, not album!)
- Set phasers to frag!

## **Bugs**
- Sleep mode causes the game and sometimes Horizon to crash. This seems to be common with ioquake3 ports and I have no idea what's causing this yet.
- Solo Match leads to a softlock at the end of every match if you're using a controller. This can be worked around by either having a USB keyboard+mouse connected, or using "Multi Match" to create a bot match instead. If you end up softlocked while playing w/ the controller, you can close the game by pressing Down to open a terminal, pressing L to bring up a virtual keyboard, typing "/quit", pressing Return, then pressing Enter twice, which should get you back to HBMenu.
- A small amount of slowdown can happen during really hectic battles in larger maps. This mostly occurs in custom maps and happens regardless of graphical settings (although dropping the resolution may help).
- If you switch between controller and keyboard + mouse input mid-match, a random input may start getting spammed (ie; your camera may start spinning wildly or your weapon may start autofiring). Just press ESC/+, click with your desired input, then press ESC/+ again and it should resolve it. 

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
seta in_gyromouse_pitch "-10"
seta in_gyromouse_yaw "-20.0"
seta in_gyromouse_pitch_ui "0.0"
seta in_gyromouse_yaw_ui "0.0"
```
## TODO

- Finish gyroscope support (80% of the way or so done, just need implement a way to implement a menu item to enable/disable gyro settings).
- Implement Switch-specific menu settings in both main menu and pause screens.
- Hopefully implement splitscreen multiplayer eventually (probably via forking parts of the Spearmint engine which will require a renderer code, controller code and menu code overhaul at minimum.)
- Release a dedicated server .nro (for no practical reason other than completion + saying I did.)


[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/donate/?cmd=_s-xclick&hosted_button_id=8GF4A3XS7ZHFY)

## **Original ReadMe**

# Tulip Voyager
**Tulip Voyager** is a fork of [Lilium Voyager](https://github.com/zturtleman/lilium-voyager) by zturtleman. As some
users have begun using this fork for custom builds it made sense to rename it to avoid confusion.

Tulip Voyager code commits: [compare/upstream_lilium...main](https://github.com/Daggolin/lilium-voyager/compare/upstream_lilium...main).
You can find the Lilium Voyager README below.

# Lilium Voyager
<img src="https://raw.githubusercontent.com/zturtleman/lilium-voyager/master/misc/lilium.png" width="64">

**Lilium Voyager** is a fork of [ioquake3](https://github.com/ioquake/ioq3) for running _Star Trek Voyager: Elite Force Holomatch_ (multiplayer). It is based on Thilo Schulz' [ioEF engine](http://thilo.tjps.eu/efport-progress/) (also known as iostvoyHM). The focus for Lilium Voyager is to maintain Elite Force multiplayer support on newer ioquake3 versions.

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


## Contributing

Please submit all patches as a GitHub pull request.

