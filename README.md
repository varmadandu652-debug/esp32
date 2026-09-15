# Device-to-Cloud Data Flow

## Project Overview

This project demonstrates a device-to-cloud data flow using MQTT.

The ESP32 simulated in Wokwi generates temperature readings and publishes
them to the public MQTT broker test.mosquitto.org.

A Python subscriber receives the readings and displays them in the terminal.

## Architecture

ESP32/Wokwi
    ↓
Temperature data
    ↓
MQTT
    ↓
test.mosquitto.org
    ↓
Python Subscriber
    ↓
Terminal / CSV file

## MQTT Configuration

Broker: test.mosquitto.org

Port: 1883

Topic: skillaudit/yourname/temp

## Running the Subscriber

Install dependencies:

pip install -r requirements.txt

Run:

python subscriber.py

## Expected Output

Connected to MQTT broker!

[2026-09-15 21:40:01] ESP32 → Temperature: 28.4 °C
[2026-09-15 21:40:04] ESP32 → Temperature: 31.2 °C
[2026-09-15 21:40:07] ESP32 → Temperature: 26.8 °C
