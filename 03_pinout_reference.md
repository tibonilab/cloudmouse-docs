# Pinout reference

### Every GPIO mapped and labeled. Encoder on pins 1-3. Display via I2C. RGB LED ready. Buzzer waiting. Your playground awaits.

Every GPIO on CloudMouse is mapped and ready to use. This reference shows you exactly which pins control what, so you can start coding immediately.

## Quick reference table

Component | Function | GPIO Pin | Notes  
---|---|---|---  
**Rotary Encoder** | CLK (A) | GPIO 16 | Rotation detection  
**Rotary Encoder** | DT (B) | GPIO 18 | Rotation direction  
**Rotary Encoder** | SW (Button) | GPIO 17 | Push button  
**RGB LED Ring** | DATA | GPIO 15 | WS2812B data line (12 LEDs)  
**Display SPI** | SCLK | GPIO 6 | SPI clock  
**Display SPI** | MOSI | GPIO 7 | SPI data out  
**Display SPI** | CS | GPIO 4 | Chip select  
**Display SPI** | DC | GPIO 5 | Data/Command select  
**Display SPI** | RST | GPIO 21 | Reset  
**Display Backlight** | BL | GPIO 8 | PWM backlight control  
**Buzzer** | Signal | GPIO 14 | Piezo buzzer output  
  
##  

## Component details

### Rotary Encoder

The encoder uses two pins (CLK and DT) for detecting rotation and direction, plus one pin for the integrated push button.

```cpp #define ENCODER_CLK_PIN 16 #define ENCODER_DT_PIN 18 #define ENCODER_SW_PIN 17 ``` 

Use interrupt-driven reading for smooth rotation detection without polling.

### RGB LED Ring

The 12 WS2812B LEDs are controlled through a single data line. Each LED can display 16.7 million colors independently.

```cpp #define NUM_LEDS 12 #define DATA_PIN 15 ``` 

Use the FastLED or Adafruit NeoPixel library for easy control.

### Display (ILI9488)

The 3.5" display uses SPI for communication. The backlight is PWM-controlled for adjustable brightness.

```cpp // SPI Configuration #define TFT_SCLK 6 #define TFT_MOSI 7 #define TFT_CS 4 #define TFT_DC 5 #define TFT_RST 21 #define TFT_BL 8 // Display specs #define SCREEN_WIDTH 480 #define SCREEN_HEIGHT 320 ``` 

We recommend using LovyanGFX library for optimal performance with the ILI9488.

### Buzzer

The piezo buzzer can play tones between 1kHz and 4kHz. Perfect for beeps, alerts, and simple melodies.

```cpp #define BUZZER_PIN 14 ``` 

Use the tone() function or PWM for generating sounds.

## Important notes

  * All GPIOs operate at 3.3V logic level
  * The display uses HSPI_HOST (SPI2)
  * VSPI_HOST (SPI3) remains available for external devices
  * USB pins (GPIO 19, 20) are reserved for USB communication
  * Some pins have internal pull-ups/pull-downs - check ESP32-S3 datasheet for details

## Adding external components

CloudMouse doesn't expose additional GPIO pins by default, keeping the design clean and compact. If you need to add external sensors or actuators, you'll need to modify the hardware or use I2C/SPI communication on the available buses.

For most projects, the onboard peripherals (display, encoder, LEDs, buzzer) provide everything you need.

## What's next?

Ready to start coding? Check out the Example Code section for ready-to-run sketches that demonstrate how to use each component.

Need library recommendations? See the Downloads section for tested Arduino libraries.