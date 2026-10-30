# Chris's Typeractive Corne Wireless — ZMK config

Branch `corne` = the 42-key Corne (6-col, nice!nano v2, no nice!view). The `lily58` branch is the Lily58.

- `config/corne.keymap` — layers and combos
- `config/corne.conf` — Bluetooth stability, sleep, Studio
- Every push builds firmware: **Actions** tab → latest run on `corne` → **firmware** zip

Flash: double-tap the reset button on a half (or hold both middle thumbs + bottom outer corner key), drag the
matching `.uf2` onto the NICENANO drive. First time: `settings_reset` on both halves, then left/right.
