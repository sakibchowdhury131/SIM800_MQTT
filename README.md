# SIM800_MQTT

An Arduino MQTT library and demo for publishing sensor data to an MQTT broker over a GSM/GPRS cellular connection using the SIM800/SIM900 module. Includes a hand-rolled MQTT protocol implementation in C++ and a demo sketch that publishes DHT sensor readings (or dummy data) in JSON format.

## Features

- Custom C++ MQTT library (`mqtt.cpp`/`mqtt.h`) implementing CONNECT, PUBLISH, and DISCONNECT messages at the byte level — no external MQTT library required
- Works with SIM800/SIM900 GSM modules over serial (AT commands)
- Demo sketch in `MQTTSIM900/` that publishes DHT sensor data (or placeholder values) as JSON to an MQTT broker
- JSON-formatted payloads for easy downstream processing

## Tech Stack

- C++ (Arduino)
- SIM800 / SIM900 GSM module
- MQTT protocol (custom implementation)
- DHT sensor (optional, replaceable with dummy data)

## Project Structure

| File / Directory | Description |
|---|---|
| `mqtt.cpp` | MQTT protocol implementation: CONNECT, PUBLISH, DISCONNECT packet builders |
| `mqtt.h` | Header file for the MQTT library |
| `MQTTSIM900/` | Arduino sketch demonstrating MQTT publish over SIM900 GSM module |

## Requirements

- Arduino IDE
- SIM800 or SIM900 GSM module
- DHT sensor (optional — dummy values work without hardware)
- MQTT broker (e.g., Mosquitto on a local server or a cloud broker)

## Usage

1. Open the sketch in `MQTTSIM900/` in the Arduino IDE.
2. Configure the broker IP, port, client ID, topic, and APN for your SIM carrier.
3. Upload to your Arduino board and open the Serial Monitor to verify connection.

## License

MIT
