# Remote Device Control via Telegram Bot
ESP32 GPIO + Raspberry Pi Zero W + Telegram Integration

## Overview
This project started in my dorm room as a DIY home automation solution using a [Raspberry Pi Zero W][(#sample-section](https://github.com/jackshisd/Pi-Zero-Server)). Initially, I hosted a Next.js web server on the Pi to monitor system status and control servos for powering on devices like my laptop or room lights. The frontend was built in JavaScript, and the backend logic was handled in Python.

To enhance portability and security, I later migrated to a Telegram bot-based system using an ESP32.

## Evolution of the Project
### Original (Raspberry Pi Web Server)
Device: Raspberry Pi Zero W

Frontend: Next.js (JavaScript)

Backend: Python

Functions:

Display Pi system status (CPU, RAM, etc.)

Control servo to physically press buttons (e.g., laptop power, light switch)

Security: Password protection for HTTP routes

### Upgraded (ESP32 + Telegram Bot)
Device: ESP32 connected to school Wi-Fi

Control Interface: Telegram Bot

Functions:

Send bot commands from phone to toggle GPIO pins

GPIO controls a relay or transistor to power on devices remotely

Advantages:

Mobile-friendly control

Works over internet without exposing a web server

Secure via Telegram’s built-in user authentication

## How It Works
Telegram Bot is set up using BotFather

ESP32 connects to Wi-Fi and polls Telegram API for new messages

Based on the message, ESP32 triggers GPIO pins

GPIO signal controls devices like laptop power via relay/servo

## Technologies Used
ESP32 (Arduino framework)

Telegram Bot API

### Previous Design

Python (Raspberry Pi backend)

Next.js (Raspberry Pi frontend)

GPIO for hardware control

Wi-Fi for remote connectivity

## Security
Only authorized Telegram users can issue commands

No open ports—communication is encrypted through Telegram

### Previous Design

Original Pi web server used password authentication before deprecation

## Future Improvements
Add status reporting (e.g. “laptop is now on”)

Add OTA updates for ESP32 firmware

Expand Telegram bot to support multiple commands/devices

Integrate camera feed from Pi Zero W

#Photos
