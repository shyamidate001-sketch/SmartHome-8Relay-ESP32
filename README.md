
# Smart Home Automation - 8-Channel Relay (ESP32)

This repository contains two demo projects for controlling an **8-channel relay** with an **ESP32**:

1. `ESP32_WebServer_8Relay` - Local web server to control 8 relays from a browser (works in STA or AP mode).
2. `ESP32_MQTT_8Relay` - MQTT-based control to integrate with Home Assistant / Node-RED (example publisher & subscriber).

---
## Important Notes / Disclaimer
- These are **demo reference implementations**. Hardware behavior depends on your relay module wiring, power supply, and relay type (active-low/active-high).
- I cannot guarantee "100% success" because physical wiring, relay current ratings, power supply quality, and level-shifting needs vary between setups. Follow wiring and safety notes below.
- Test on a bench with no mains connected to relay contacts first. Use low-voltage devices for initial tests.

---
## Common Wiring (8-channel relay module)
- Relay VCC -> 5V (or 3.3V depending on your relay board; check the board).
- Relay GND -> ESP32 GND.
- Relay IN1..IN8 -> ESP32 GPIO pins listed in the examples.
- If relay requires 5V logic, use a level shifter or a relay module with opto-isolation that accepts 3.3V inputs.
- DO NOT power ESP32 from relay VCC if the relay board draws large current. Use separate regulated supplies and common ground.

---
## Files included
- `ESP32_WebServer_8Relay/ESP32_8Relay_WebServer.ino` - Web server project.
- `ESP32_MQTT_8Relay/ESP32_8Relay_MQTT.ino` - MQTT control example.
- `README.md` - this file
- `WIRING.md` - quick wiring guide
---
