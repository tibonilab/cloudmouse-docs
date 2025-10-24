# Downloads & Files

### Grab firmware binaries. Schematics in PDF. PCB layouts. 3D case files. Pinout diagrams. Arduino libraries. USB drivers. Everything you need. Free.

Everything you need in one place. Firmware binaries, hardware files, libraries, drivers, and documentation. All free, all open source (except the trademarked enclosure design).

## Firmware

### Boilerplate Firmware

The official Hello World firmware. Tests all hardware components and serves as a starting point for your projects.

  * **Source Code:** [github.com/cloudmouse-co/boilerplate](https://github.com/cloudmouse-co/boilerplate)
  * **Pre-compiled Binary:** cloudmouse-boilerplate-v1.0.bin
  * **Flash Instructions:** See Getting Started guide

### Asteroids Firmware

The game that ships pre-loaded on CloudMouse. Easter egg that makes you smile.

  * **Source Code:** github.com/cloudmouse-co/asteroids
  * **Pre-compiled Binary:** cloudmouse-asteroids-v1.0.bin

### Example Firmwares

All example projects as ready-to-flash binaries. No compilation needed.

  * **LED Animations:** led-animations.bin
  * **WiFi Scanner:** wifi-scanner.bin
  * **BLE Mouse:** ble-mouse.bin
  * **Web Server:** web-server.bin
  * **Sensor Dashboard:** sensor-dashboard.bin
  * **Menu System:** menu-system.bin

## Hardware Files

### Schematics

Complete electrical schematics in PDF format. See exactly how CloudMouse is wired.

  * **Main Schematic:** cloudmouse-schematic-v1.0.pdf
  * **Power Circuit:** cloudmouse-power-schematic.pdf
  * **Display Circuit:** cloudmouse-display-schematic.pdf

### PCB Files

PCB layouts in KiCad format. Modify, remix, manufacture your own.

  * **KiCad Project:** cloudmouse-pcb-kicad.zip
  * **Gerber Files:** cloudmouse-gerbers-v1.0.zip
  * **BOM (Bill of Materials):** cloudmouse-bom-v1.0.csv

### Pinout Diagrams

Visual pinout references for quick lookup.

  * **Full Pinout Diagram:** cloudmouse-pinout.pdf
  * **Display Pinout:** cloudmouse-display-pinout.pdf
  * **High-res PNG:** cloudmouse-pinout.png

## Software & Libraries

### Arduino Libraries

Recommended libraries for CloudMouse development. Install via Arduino Library Manager or download manually.

  * **LovyanGFX:** Display graphics library (recommended for ILI9488)
  * **FastLED:** RGB LED control and effects
  * **ESP32Encoder:** Rotary encoder handling
  * **ArduinoJson:** JSON parsing for web/API projects
  * **ESPAsyncWebServer:** Async web server for better performance

All libraries are available through Arduino Library Manager. Search by name and install.

### USB Drivers

Most modern systems auto-detect ESP32-S3. If your computer doesn't recognize CloudMouse, install these drivers:

  * **Windows:** [CP210x USB Driver](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers)
  * **macOS:** Usually works without drivers. If not, install CP210x driver above
  * **Linux:** Built-in kernel support. No drivers needed

## Documentation

### PDF Guides

Offline versions of this documentation for reading without internet.

  * **Complete Documentation:** cloudmouse-docs-complete.pdf
  * **Getting Started Guide:** cloudmouse-getting-started.pdf
  * **Hardware Reference:** cloudmouse-hardware-reference.pdf

### Datasheets

Component datasheets for deep-dive technical reference.

  * **ESP32-S3:** [ESP32-S3 Datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf)
  * **ILI9488 Display:** ili9488-datasheet.pdf
  * **WS2812B LEDs:** ws2812b-datasheet.pdf

## 3D Files

The CloudMouse enclosure design is trademarked and not available for download. This protects the distinctive CloudMouse design and brand identity.

If you need a custom enclosure for a specific project, consider designing your own or contact us for OEM/partnership opportunities.

## Development Tools

### Arduino IDE

Official Arduino IDE for CloudMouse development.

  * **Download:** [arduino.cc/en/software](https://www.arduino.cc/en/software)
  * **Version:** 2.x or newer recommended

### ESP32 Board Package

Add ESP32 support to Arduino IDE.

  * **Board Manager URL:** `https://espressif.github.io/arduino-esp32/package_esp32_index.json`
  * **Installation:** See Getting Started guide for detailed instructions

### Git

Version control for cloning repositories and managing code.

  * **Download:** [git-scm.com](https://git-scm.com)
  * **GUI Options:** GitHub Desktop, GitKraken, SourceTree (optional)

## Flash Tools

### ESP Flash Download Tool

Official Espressif tool for flashing pre-compiled binaries without Arduino IDE.

  * **Download:** [Espressif Flash Download Tool](https://www.espressif.com/en/support/download/other-tools)
  * **Use case:** Flash .bin files directly without compiling source code

### esptool.py

Command-line tool for flashing ESP32 devices. For advanced users.

  * **Install:** `pip install esptool`
  * **Flash command:** `esptool.py --chip esp32s3 write_flash 0x0 firmware.bin`

## License Information

Before using these files, understand the licensing:

  * **Firmware & Software:** MIT License (permissive, commercial use OK)
  * **Hardware (PCB/Schematics):** CERN OHL (permissive, commercial use OK)
  * **Enclosure Design:** Trademarked, not open source
  * **Documentation:** Creative Commons BY-SA 4.0

You can use, modify, and sell products based on CloudMouse electronics and software. Just give credit and share modifications. Cannot reproduce the trademarked enclosure design.

## Need something not listed?

Missing a file or resource? Let us know on Discord or GitHub. We're constantly adding new downloads and resources based on community needs.