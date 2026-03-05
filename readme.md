# ZMK CONFIG FOR THE CHARYBDIS 4X6 WIRELESS SPLIT KEYBOARD

keymap editor https://nickcoutsos.github.io/keymap-editor/

## ZMK Studio — keyboard in "Select device" (Bluetooth)

To have your Charybdis show up when you click **Select device** in the ZMK Studio desktop app over **Bluetooth** (no need to "add config"):

1. **Build** — Push this repo so GitHub Actions runs, or build locally. Ensure the build **succeeds**.
2. **Download** the **right-half** firmware (the one built with ZMK Studio):
   - From Actions: artifact like `charybdis_right-nice_nano__zmk-zmk.uf2` (or similar from the firmware archive).
3. **Flash** that `.uf2` to the **right** half of the keyboard (the central half that handles BLE).
4. **Pair** the keyboard with your computer via Bluetooth (system Bluetooth settings).
5. Open ZMK Studio → **Select device**. Your Charybdis should appear in the list as a BLE device.

The left half stays on the normal (non-Studio) firmware; only the right (central) half needs the Studio build. If the keyboard is also connected via USB, switch its output to BLE (e.g. `&out OUT_BLE`) so Studio talks to it over Bluetooth.

## BOM

Here is the BOM for this project: [BOM Charybdis 4x6 Wireless](/docs/bom/readme.md)

![Tim Keyboard](/docs/picture/20250423-_DSC1557.jpg)

## Keymap

This is iamtienng's keymap for Charybdis
Generated with [Keymap Drawer](https://github.com/caksoylar/keymap-drawer-web/)
![Tim Keymap](/docs/keymap/tim_keymap.svg)
