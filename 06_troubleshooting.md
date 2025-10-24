# Troubleshooting

### Device not found? Try different cable. Upload fails? Hold BOOT button. Display blank? Check I2C address. We've been there. Solutions inside.

Something not working? Don't panic. Most issues have simple solutions. We've collected the most common problems and their fixes here.

## Device not recognized by computer

**Symptoms:** Computer doesn't detect CloudMouse when plugged in. No COM port appears in Arduino IDE.

**Solutions:**

  * Try a different USB-C cable. Some cables are power-only and don't support data transfer
  * Try a different USB port on your computer. Some USB hubs don't work well with ESP32
  * On Windows: Check Device Manager for unknown devices or devices with yellow warning icons
  * Install or update USB drivers for ESP32-S3 (CH340 or CP2102 depending on your board revision)
  * Restart your computer. Sometimes USB drivers get stuck

## Upload fails or times out

**Symptoms:** Arduino IDE shows "Failed to connect" or "Timed out waiting for packet header" during upload.

**Solutions:**

  * Hold the BOOT button on CloudMouse while clicking Upload in Arduino IDE
  * Keep holding BOOT until you see "Connecting..." message
  * Release BOOT button after upload starts (when you see percentage progress)
  * Make sure you selected the correct COM port in Tools → Port
  * Try lowering upload speed: Tools → Upload Speed → 115200 or 460800
  * Close Serial Monitor if it's open (it blocks the COM port)

## Display stays blank or white

**Symptoms:** Screen doesn't show anything after upload. Display is completely white or black.

**Solutions:**

  * Check that you're using the correct display library (LovyanGFX for ILI9488)
  * Verify pin configuration matches the Pinout Reference (SCLK=6, MOSI=7, CS=4, DC=5, RST=21, BL=8)
  * Check that backlight is enabled in code. Try setting backlight to maximum: `lcd.setBrightness(255);`
  * Make sure PSRAM is enabled in Arduino IDE settings (Tools → PSRAM → OPI PSRAM)
  * Try the boilerplate firmware from Hello World guide to verify hardware works

## LEDs don't light up

**Symptoms:** RGB LED ring stays dark even when code uploads successfully.

**Solutions:**

  * Verify you're using DATA_PIN 15 in your FastLED configuration
  * Check LED type is set to WS2812B with GRB color order
  * Try increasing brightness: `FastLED.setBrightness(100);`
  * Make sure you're calling `FastLED.show();` after setting LED colors
  * Test with simple code that lights all LEDs to one color

## Encoder not responding

**Symptoms:** Rotating encoder or pressing button doesn't trigger any action.

**Solutions:**

  * Verify pin configuration: CLK=16, DT=18, SW=17
  * Use interrupt-driven reading instead of polling for better responsiveness
  * Add debouncing to button reads (wait 50ms after detecting press)
  * Check that you configured pins as INPUT_PULLUP for the button
  * Test encoder with Serial.println() to verify it's actually being read

## Buzzer doesn't make sound

**Symptoms:** Buzzer stays silent when code tries to play tones.

**Solutions:**

  * Verify buzzer pin is set to GPIO 14
  * Use frequencies between 1kHz and 4kHz (piezo buzzer optimal range)
  * Try simple tone() function: `tone(BUZZER_PIN, 2000, 500);`
  * Make sure pin is configured as OUTPUT
  * Check that other code isn't using the same pin or PWM channel

## WiFi connection fails

**Symptoms:** CloudMouse can't connect to WiFi network. WiFi.status() stays WL_DISCONNECTED.

**Solutions:**

  * Double-check SSID and password (case-sensitive)
  * Make sure your network is 2.4GHz (ESP32 doesn't support 5GHz)
  * Move closer to WiFi router during testing
  * Try connecting to WiFi hotspot from phone to verify WiFi hardware works
  * Add delay after WiFi.begin() to give it time to connect: `delay(5000);`
  * Check that WiFi antenna isn't blocked or damaged

## Code compiles but crashes immediately

**Symptoms:** Upload succeeds but device reboots constantly or doesn't respond. Serial Monitor shows crash messages or boot loops.

**Solutions:**

  * Enable USB CDC On Boot in Arduino IDE settings (Tools → USB CDC On Boot → Enabled)
  * Make sure Flash Size is set to 16MB in Tools menu
  * Verify PSRAM is configured as OPI PSRAM in Tools menu
  * Check that you're not running out of memory (add Serial.println(ESP.getFreeHeap()) to debug)
  * Reduce image sizes or move large data to PSRAM or flash storage
  * Comment out sections of code to isolate what's causing the crash

## Serial Monitor shows garbage characters

**Symptoms:** Serial Monitor displays random characters or symbols instead of readable text.

**Solutions:**

  * Set baud rate to 115200 in both code and Serial Monitor
  * Make sure "Both NL & CR" or "Newline" is selected in Serial Monitor dropdown
  * Close and reopen Serial Monitor
  * Try pressing the RST button on CloudMouse after opening Serial Monitor

## Still having problems?

If none of these solutions work:

  * Check the GitHub Issues page for your specific example or firmware
  * Join our Discord community and ask for help (include error messages and what you've already tried)
  * Post on the community forum with detailed description and photos if relevant
  * Make sure you're using the latest version of Arduino IDE and ESP32 board package

When asking for help, include:

  * What you're trying to do
  * What's happening instead
  * Arduino IDE version and ESP32 board package version
  * Full error messages from Arduino IDE
  * Your board configuration settings

The more information you provide, the faster we can help you solve the problem.