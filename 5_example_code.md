Ready-to-run examples that show you what CloudMouse can do. Each example is complete, documented, and available on GitHub. Pick one, clone it, upload it, and see it work.

All examples are built to teach you something specific while being actually useful. No toy projects here.

## Available examples

### 1\. LED Animations

**What it does:** Multiple LED effects including rainbow cycle, breathing, scanner, and theater chase. Use the encoder to switch between animations and adjust speed.

**What you'll learn:**

  * Advanced FastLED effects and color manipulation
  * Smooth animations with proper timing
  * Encoder input for UI control
  * Display feedback for current mode

**GitHub:** [cloudmouse-co/example-led-animations](https://github.com/cloudmouse-co/example-led-animations)

### 2\. WiFi Scanner

**What it does:** Scans for WiFi networks and displays them on screen with signal strength bars. Shows SSID, channel, encryption type, and RSSI. Auto-refreshes every few seconds.

**What you'll learn:**

  * WiFi scanning and network detection
  * Parsing WiFi information (SSID, RSSI, encryption)
  * Dynamic list rendering on display
  * Signal strength visualization

**GitHub:** [cloudmouse-co/example-wifi-scanner](https://github.com/cloudmouse-co/example-wifi-scanner)

### 3\. BLE HID Mouse

**What it does:** Turns CloudMouse into a wireless Bluetooth mouse. Rotate the encoder to move cursor, press button to click. Works with any device that supports BLE HID.

**What you'll learn:**

  * Bluetooth Low Energy HID protocol
  * HID mouse report format
  * Encoder as input device
  * BLE pairing and connection handling

**GitHub:** [cloudmouse-co/example-ble-mouse](https://github.com/cloudmouse-co/example-ble-mouse)

### 4\. Web Server Dashboard

**What it does:** Creates a local web server with a control panel. Access it from your browser to control LEDs, display messages, read sensor data, and trigger buzzer. Perfect starting point for IoT projects.

**What you'll learn:**

  * ESP32 web server basics
  * HTML/CSS/JavaScript interface design
  * AJAX requests for real-time updates
  * JSON data exchange
  * Access Point and Station modes

**GitHub:** [cloudmouse-co/example-web-server](https://github.com/cloudmouse-co/example-web-server)

### 5\. Sensor Dashboard

**What it does:** Displays real-time system information: WiFi signal strength, free memory, uptime, CPU temperature. Updates every second with animated graphs. Great template for monitoring projects.

**What you'll learn:**

  * Reading ESP32 internal sensors
  * Real-time data visualization
  * Simple graph rendering
  * System monitoring and diagnostics

**GitHub:** [cloudmouse-co/example-sensor-dashboard](https://github.com/cloudmouse-co/example-sensor-dashboard)

### 6\. Encoder Menu System

**What it does:** Full menu system with encoder navigation. Multiple screens, submenus, settings, value adjustment. Shows how to build complex UIs with just a rotary encoder and display.

**What you'll learn:**

  * Menu system architecture
  * State management for UI
  * Encoder-based navigation patterns
  * Drawing menus and selection indicators

**GitHub:** [cloudmouse-co/example-menu-system](https://github.com/cloudmouse-co/example-menu-system)

## How to use these examples

**Step 1:** Choose an example from the list above

**Step 2:** Clone the repository

```bash git clone [repository-url] cd [repository-name] ``` 

**Step 3:** Open the `.ino` file in Arduino IDE

**Step 4:** Read the README.md for specific instructions and dependencies

**Step 5:** Install any required libraries (listed in the README)

**Step 6:** Upload to your CloudMouse and test

Each example includes detailed comments explaining how the code works. Use them as learning material or as starting points for your own projects.

## Modifying examples

These examples are meant to be modified and adapted. Here's how to get started:

  * Fork the repository on GitHub
  * Make your changes locally
  * Test on your CloudMouse
  * Commit and push to your fork
  * Share your modifications with the community

Found a bug or have an improvement? Open an issue or submit a pull request on GitHub.

## Need help?

Having trouble with an example? Check the repository's Issues page on GitHub. Someone might have already solved your problem.

Still stuck? Join our Discord community for help from other makers.

## Want more examples?

The community is constantly creating new examples. Check the CloudMouse GitHub organization for the latest projects.

Built something cool? Share it! We love featuring community projects.