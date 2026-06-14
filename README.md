# MichelFR TeslaMate Home Assistant Add-on

A Home Assistant add-on repository containing **TeslaMate**, bumped to the latest
upstream TeslaMate release.

This is a fork/restructure of [lildude/ha-addon-teslamate](https://github.com/lildude/ha-addon-teslamate)
packaged as an add-on repository so it can be added directly to Home Assistant.

## Add-ons

### TeslaMate

- TeslaMate version: **4.0.1**
- Built locally by the Supervisor (no prebuilt image), so this exact version is used.
- Uses an **external** PostgreSQL database (the Home Assistant PostgreSQL add-on),
  Grafana and Mosquitto — your car data lives in PostgreSQL, not in the add-on.

## Install

1. Settings → Add-ons → Add-on Store → ⋮ → Repositories.
2. Add: `https://github.com/MichelFR/ha-addon-teslamate`
3. Install **TeslaMate**, configure the database / MQTT / encryption key options,
   then start it.

> Switching from another TeslaMate add-on: point this one at the **same** database
> and use the **same** `encryption_key` so your history and stored Tesla tokens are
> reused. Do not run two TeslaMate instances against the same database at once.
> TeslaMate 4.0.1 applies forward database migrations on first start — take a
> PostgreSQL backup before switching, as downgrades are not supported.

Credit: original add-on by [Colin Seymour (lildude)](https://github.com/lildude). MIT licensed.
