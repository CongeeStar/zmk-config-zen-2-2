# Lily58 (54-key wireless split) — ZMK config

This branch (`lily58`) holds the firmware config for the AliExpress "Lily58" wireless split
(nice!nano v2 clone controllers, 27 keys per side). The `main` branch is the separate
Corneish Zen config and is untouched.

- `config/lily58.keymap` — the layout, layers and combos
- `config/lily58.conf` — settings (radio power, sleep)
- `build.yaml` — what GitHub builds: left (with ZMK Studio), right, settings_reset
- ZMK is pinned to v0.3

## Getting firmware
Every push to this branch builds automatically: **Actions** tab → latest run on `lily58`
→ download the **firmware** zip at the bottom.

## Flashing (each half separately, over USB)
1. Enter bootloader: hold **FN (Nav) + right layer thumb** + top-left key (left half) or top-right key (right half). Left half only: **FN + top-left key**.
   Fallback: short RST to GND twice quickly with tweezers.
2. Drag the matching `.uf2` onto the drive that appears (NICENANO).
   - `lily58_left ... .uf2` → left half
   - `lily58_right ... .uf2` → right half
3. First time only: flash `settings_reset` to both halves first, then the real files,
   then turn both halves off and on together and re-pair in Windows Bluetooth.
