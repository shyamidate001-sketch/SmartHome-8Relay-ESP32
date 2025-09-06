
# Wiring Quick Guide

Recommended test pins (change in code if you prefer different pins):

GPIO mapping (example):
- RELAY 1 -> GPIO 16
- RELAY 2 -> GPIO 17
- RELAY 3 -> GPIO 5
- RELAY 4 -> GPIO 18
- RELAY 5 -> GPIO 19
- RELAY 6 -> GPIO 21
- RELAY 7 -> GPIO 22
- RELAY 8 -> GPIO 23

Steps:
1. Power the relay module separately with a stable 5V supply if required. Connect grounds together.
2. Connect IN pins to the ESP32 GPIOs listed above.
3. Upload the sketch and open Serial Monitor at 115200 baud to see IP address and status.
4. Open the IP in browser, or connect to the ESP32 AP if STA fails.

Safety:
- When switching mains loads, ensure the relay contacts and wiring meet current/voltage requirements.
- If unsure, consult an electrician for mains wiring.
