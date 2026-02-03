# Arduino Ultrasonic Distance Sensor (Uno R4 WiFi)

## Project
Simple distance measurement project using an HC-SR04 (or compatible) ultrasonic sensor with the `Arduino Uno R4 WiFi` board. The sketch reads distance and prints it to the serial monitor.

## Files
- `src/main.cpp` — Arduino sketch that triggers the sensor and calculates distance.
- `platformio.ini` — PlatformIO configuration for building and uploading to the `Arduino Uno R4 WiFi`.

## Hardware
- Arduino Uno R4 WiFi
- Ultrasonic sensor (HC-SR04 or compatible)
- Jumper wires
- Breadboard (optional)
- 5V power from the board

Wiring (pins used in `src/main.cpp`):
- Trig pin -> digital pin 9 (`trigPin`)
- Echo pin -> digital pin 10 (`echoPin`)
- VCC -> 5V
- GND -> GND

## Software / Dependencies
- PlatformIO (recommended) or Arduino IDE
- Board: `Arduino Uno R4 WiFi`
- Serial monitor baud rate: `9600`

## Build & Upload (PlatformIO)
1. Open the project in your editor (CLion with PlatformIO or VS Code with PlatformIO extension).
2. Ensure `platformio.ini` is configured for the `arduino_uno_r4_wifi` board.
3. Build: `pio run`
4. Upload: `pio run --target upload`
5. Open serial monitor: `pio device monitor -b 9600`

## Expected Output
Serial monitor displays distance readings, e.g.:
Distance: 23 cm

## Troubleshooting
- No output on serial monitor: check baud rate is `9600` and correct COM port is selected.
- Readings unchanged or unstable: verify wiring, ensure `Echo` and `Trig` pins match `src/main.cpp`, and sensor has clear line-of-sight.
- If using a 3.3V tolerant board variant, confirm sensor power levels are compatible.

## License
MIT — adapt as needed.
