# IR Server Telnet Home Assistant Integration

Home Assistant custom integration for [IR Server Telnet](https://github.com/devprbtt/ir-server-esp32).

This integration connects to the ESP32 firmware over the local telnet/HTTP APIs and provides:
- climate entities for standard HVAC device profiles
- button entities for custom profile commands
- diagnostic sensors for firmware status, heap, RSSI, version state, and connectivity
- Zeroconf discovery through the firmware's `_hvactelnet._tcp.local.` mDNS service

## Repository layout
- `custom_components/hvactelnet/`: install this folder into your Home Assistant `custom_components` directory

## Install
Copy `custom_components/hvactelnet` into your Home Assistant config directory:

```text
config/
  custom_components/
    hvactelnet/
```

Then restart Home Assistant.

## Discovery
If the firmware is already running on your network and this integration is installed, Home Assistant should discover the device automatically.

## Notes
- The integration domain remains `hvactelnet` for compatibility with existing installs.
- The firmware project and API documentation live in the firmware repository:
  https://github.com/devprbtt/ir-server-esp32
