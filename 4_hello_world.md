Your first complete CloudMouse program. This firmware tests all the hardware at once: display shows instructions, LEDs pulse gently, encoder detects rotation and clicks, buzzer beeps on button press.

Perfect for verifying that everything works and learning how to use Git, clone repositories, and flash firmware to your CloudMouse.

## Before you start

Make sure you have Arduino IDE installed and configured to communicate with your CloudMouse. If you haven't done this yet, go to the Getting Started guide first.

## What this firmware does

  * **Display:** Shows "Hello CloudMouse!" and real-time instructions
  * **LED ring:** Pulses smoothly while waiting for input
  * **Encoder rotation:** Display shows "Rotating LEFT" or "Rotating RIGHT"
  * **Encoder button:** Display shows "Button pressed!", buzzer beeps, LEDs flash
  * **Serial output:** Prints all events for debugging

This is the perfect way to verify that all your hardware is working correctly.

## Step 1: Install Git

If you don't have Git installed, download it from [git-scm.com](https://git-scm.com)

Verify installation by opening a terminal and typing:

```bash git --version ``` 

## Step 2: Clone the repository

Open a terminal and navigate to where you want to save the project. Then clone the CloudMouse boilerplate repository:

```bash git clone https://github.com/cloudmouse-co/boilerplate.git cd boilerplate ``` 

This downloads the complete firmware with all necessary files and libraries.

## Step 3: Open in Arduino IDE

Launch Arduino IDE and open the project:

File -> Open -> Navigate to the cloned folder -> Select the `.ino` file

Arduino IDE will open the project with all its files.

## Step 4: Verify board configuration

Double-check your Arduino IDE settings match these values:

  * Board: ESP32S3 Dev Module
  * USB CDC On Boot: Enabled
  * Flash Size: 16MB
  * PSRAM: OPI PSRAM
  * Port: Your CloudMouse COM port

If you're not sure about these settings, check the Getting Started guide.

## Step 5: Build and upload

Connect your CloudMouse via USB-C and click the Upload button in Arduino IDE.

The firmware will compile and upload to your device. This might take a minute or two the first time.

If upload fails, try holding the BOOT button on your CloudMouse while clicking Upload, then release it after the upload starts.

## Step 6: Test your CloudMouse

After upload completes, your CloudMouse will restart and you'll see:

  * Display showing "Hello CloudMouse!" with instructions
  * LED ring pulsing gently
  * Rotate the encoder: display updates with direction
  * Press the encoder button: buzzer beeps, LEDs flash, display confirms

Open the Serial Monitor (Tools -> Serial Monitor, set to 115200 baud) to see detailed debug output.

## Understanding the code

The boilerplate firmware is organized in clear sections:

  * **Hardware initialization:** Display, LEDs, encoder, buzzer setup
  * **Display rendering:** How to draw text and graphics on screen
  * **LED animations:** Smooth pulsing effect using FastLED
  * **Encoder reading:** Interrupt-driven rotation and button detection
  * **Event handling:** How to respond to user input

Browse the code to see how each component works. Every section is commented and easy to understand.

## What's next?

Now that you've flashed your first complete firmware, you can:

  * Modify the code to customize behavior
  * Check out the Example Code section for more advanced projects
  * Read the Pinout Reference to understand all available hardware
  * Build your own projects starting from this boilerplate

The boilerplate is designed to be your starting point. Fork it, modify it, break it, fix it. It's yours.

Congratulations! You've successfully built and flashed CloudMouse firmware. You're officially a CloudMouse developer now.