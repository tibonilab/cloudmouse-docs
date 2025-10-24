# Hardware specs

### Dual-core ESP32-S3 running at 240MHz. 8MB PSRAM for your ideas. 16MB flash for your code. Plus encoder, display, LED, buzzer.

CloudMouse is built around the ESP32-S3 N16R8, a powerful dual-core microcontroller with integrated WiFi and Bluetooth. Everything you need to build interactive projects is already on board.

## Microcontroller

**ESP32-S3 N16R8**

  * CPU: Xtensa 32-bit LX7 dual-core @ 240 MHz
  * Flash Memory: 16MB
  * PSRAM: 8MB (OPI)
  * Architecture: Xtensa LX7 with FPU and vector instructions

## Wireless connectivity

**WiFi**

  * Standard: 802.11 b/g/n (WiFi 4)
  * Frequency: 2.4 GHz
  * Modes: AP, STA, AP+STA, WiFi Direct
  * Security: WPA2-Enterprise, WPA3-SAE

**Bluetooth**

  * Version: Bluetooth 5 (LE + Classic)
  * Profiles: BLE HID, BLE GATT, iBeacon, Eddystone, A2DP, SPP
  * Range: Up to 10 meters (depending on environment)

**ESP-NOW**

  * Low-latency ESP-to-ESP communication protocol
  * Perfect for mesh networks and multi-device projects

## Display

**3.5 " TFT-LCD IPS**

  * Resolution: 320 x 480 pixels
  * Interface: SPI
  * Controller IC: ILI9488
  * Color Depth: 24-bit RGB (16.7 million colors)
  * Viewing angles: Wide (IPS technology)

## Input devices

**Rotary encoder**

  * Type: Incremental rotary encoder
  * Resolution: 18 pulses per revolution
  * Integrated push-button
  * Perfect for menu navigation and value adjustment

## Output devices

**RGB LED Ring**

  * Type: WS2812B addressable RGB LEDs
  * Count: 12 LEDs in circular arrangement
  * Color Depth: 24-bit per LED (RGB 8-8-8)
  * Individual control of each LED

**Buzzer**

  * Type: Piezoelectric buzzer
  * Frequency range: 1 kHz to 4 kHz
  * Use for audio feedback, alerts, simple melodies

## Power and connectivity

**USB-C**

  * Standard: USB 2.0 Full-Speed (12 Mbps)
  * Power Input: 5V / 1A
  * USB OTG support
  * Used for programming, power, and USB HID communication

## Physical specifications

  * Dimensions: 183.5x101.7x63.2 cm
  * Weight: 280gr
  * Operating temperature: 0°C to 60°C

## What can you do with this hardware?

The combination of display, encoder, LEDs, and wireless connectivity makes CloudMouse perfect for:

  * Custom wireless input devices (mouse, keyboard, game controller)
  * IoT dashboards with real-time data visualization
  * Interactive art installations with LED animations
  * Network tools (WiFi scanner, packet sniffer, network monitor)
  * Smart home controllers with visual feedback
  * Learning platform for embedded systems programming

With 16MB of flash and 8MB of PSRAM, you have plenty of space for complex applications, graphics, and data storage.

Want to see how everything connects? Check the Pinout Reference for detailed GPIO mapping.