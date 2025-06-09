<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/TOTEM_logo_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/TOTEM_logo_bright.svg">
  <img alt="TOTEM logo font" src="/docs/images/TOTEM_logo_bright.svg">
</picture>

# Sandy's custom Totem Layout

This is a custom layout for the totem split keyboard. Full readme from the creator below.

The base of the layout is a QWERTY [Miryoku](https://github.com/manna-harbour/miryoku/) layout, but I diverged from their base implementation for better support of modifications.
This layout makes liberal use of [Urob's](https://github.com/urob) excellent helpers and modules, with some ideas taken from his personal config.

Ideas include:
  - Timeless Homerow mods
  - Multi-function shift key
  - Combos for symbols

This all builds fine via GitHub Actions.

[!NOTE]
I may implement the tri-state tab shifter in the future

[!WARNING]
I was unable to get Urob's hack for allowing the homerow combos to be tap only, this doesn't have much impact on daily use but would be wise to keep and eye on ZMK Issue [#544](https://github.com/zmkfirmware/zmk/issues/544)

## ZMK CONFIG FOR THE TOTEM SPLIT KEYBOARD

[Here](https://github.com/GEIGEIGEIST/totem) you can find the hardware files and build guide.\
[Here](https://github.com/GEIGEIGEIST/qmk-config-totem) you can find the QMK config for the TOTEM.

TOTEM is a 38 key column-staggered split keyboard running [ZMK](https://zmk.dev/) or [QMK](https://docs.qmk.fm/). It's meant to be used with a SEEED XIAO BLE or RP2040.


![TOTEM layout](/docs/images/TOTEM_layout.svg)



## HOW TO USE

- fork this repo
- `git clone` your repo, to create a local copy on your PC (you can use the [command line](https://www.atlassian.com/git/tutorials) or [github desktop](https://desktop.github.com/))
- adjust the totem.keymap file (find all the keycodes on [the zmk docs pages](https://zmk.dev/docs/codes/))
- `git push` your repo to your fork
- on the GitHub page of your fork navigate to "Actions"
- scroll down and unzip the `firmware.zip` archive that contains the latest firmware
- connect the left half of the TOTEM to your PC, press reset twice
- the keyboard should now appear as a mass storage device
- drag'n'drop the `totem_left-seeeduino_xiao_ble-zmk.uf2` file from the archive onto the storage device
- repeat this process with the right half and the `totem_right-seeeduino_xiao_ble-zmk.uf2` file.
