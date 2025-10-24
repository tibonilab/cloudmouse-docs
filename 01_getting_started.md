# Getting started

### Plug in. Play Asteroids. Smile. Now install Arduino IDE, select ESP32S3, and upload your first sketch. You're a CloudMouse developer now.

Ready to start coding your CloudMouse? This guide will take you from unboxing to uploading your first sketch in minutes.

## What you need

  * Your CloudMouse device
  * A USB-C cable (data capable, not just power)
  * A computer running Windows, macOS, or Linux
  * Arduino IDE installed

## Step 1: Install Arduino IDE

Download and install Arduino IDE 2.x from the official Arduino website.

Don't have it yet? Grab it here: [arduino.cc/en/software](https://www.arduino.cc/en/software)

## Step 2: Add ESP32 board support

Open Arduino IDE and go to File -> Preferences.

In the "Additional Board Manager URLs" field, add this URL:

`https://espressif.github.io/arduino-esp32/package_esp32_index.json`

Click OK to save.

Now go to Tools -> Board -> Boards Manager. Search for "esp32" and install "esp32 by Espressif Systems".

Wait for the installation to complete. It might take a few minutes.

## Step 3: Connect your CloudMouse

Plug your CloudMouse into your computer using a USB-C cable.

Make sure the cable supports data transfer. Some cables are power-only and won't work.

Your computer should recognize the device. On Windows, it might install drivers automatically.

## Step 4: Select the board and port

In Arduino IDE, go to Tools -> Board -> esp32 -> ESP32S3 Dev Module.

Then go to Tools -> Port and select the port where CloudMouse is connected. It usually shows as:

  * Windows: COM3, COM4, or similar
  * macOS: /dev/cu.usbserial-XXXX or /dev/cu.usbmodem-XXXX
  * Linux: /dev/ttyUSB0 or /dev/ttyACM0

Now configure these critical settings in the Tools menu:

  * USB CDC On Boot: Enabled
  * Flash Size: 16MB
  * PSRAM: OPI PSRAM
  * Partition Scheme: Default 4MB with spiffs (or 16MB with FFAT if you need more storage)

## Step 5: Upload your first sketch

Copy this simple test code into Arduino IDE:

```cpp
void setup() {
  Serial.begin(115200);
  Serial.println("Hello CloudMouse!");
}

void loop() {
  Serial.println("I'm alive!");
  delay(1000);
}
```
 

Click the Upload button (arrow icon) in the toolbar.

Arduino IDE will compile and upload the code to your CloudMouse.

💡 If upload fails, try holding the BOOT button on your CloudMouse while clicking Upload, then release it after upload starts.

## Step 6: Open Serial Monitor

After upload completes, open Tools -> Serial Monitor.

Set baud rate to 115200.

You should see "Hello CloudMouse!" followed by "I'm alive!" messages every second.

Congratulations! You're officially a CloudMouse developer now.

## What's next?

Check out the Example Code section for ready-to-run projects like LED animations, display graphics, and WiFi scanning.

Want to understand the hardware? Read the Hardware Specs and Pinout Reference.

Something not working? Jump to Troubleshooting for solutions.

Now go build something awesome.