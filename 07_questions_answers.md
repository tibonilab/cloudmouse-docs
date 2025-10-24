# Questions & Answers

### What can I build? Anything controllable. Need coding skills? Basics help. Open source? Yes. Battery life? Depends on you. More answers inside.

Got questions? We've got answers. Here are the most common questions about CloudMouse, from capabilities to technical details.

## General questions

### What can I build with CloudMouse?

Anything controllable. Seriously. Custom wireless input devices (mouse, keyboard, game controllers), IoT dashboards with live data, interactive art installations, WiFi/Bluetooth scanners and sniffers, smart home controllers, network monitoring tools, learning platform for embedded programming. If you can imagine it and it involves input/output, sensors, or connectivity, CloudMouse can probably do it.

### Do I need coding skills?

Basic programming knowledge helps, but you don't need to be an expert. If you can read and modify simple C/C++ code, you're good. All our examples are heavily commented and designed to be learning tools. Start with the boilerplate firmware, modify it step by step, break things, fix them. That's how you learn.

### Is CloudMouse open source?

Yes, mostly. All firmware, schematics, PCB layouts, and code examples are fully open source and available on GitHub. However, the physical design and 3D case files are trademarked and not released publicly to protect the CloudMouse brand identity. You can modify and use all the electronics and software freely, but the distinctive CloudMouse enclosure design is protected.

### What's the license?

Hardware schematics and PCB files are licensed under CERN Open Hardware License (permissive). Software is MIT licensed. You can use CloudMouse electronics and software commercially without asking permission or paying royalties. The physical enclosure design is trademarked and cannot be reproduced. We only ask that you credit the project and share your improvements back if possible.

### Can I use CloudMouse in commercial products?

Yes, with limitations. You can use the electronics (schematics, PCB designs) and software in your commercial products. You can modify the design and sell them. However, you cannot reproduce the distinctive CloudMouse enclosure design as it's trademarked. Create your own enclosure design or significantly modify ours. Just follow the open source license terms for electronics/software (give credit, share modifications if distributing derivatives).

## Hardware questions

### Can I add external sensors or modules?

CloudMouse is designed as a wireless-first device. It communicates with other devices via WiFi and Bluetooth, not through physical GPIO pins. This is a feature, not a limitation: no cables, everything wireless. For most projects, wireless connectivity is all you need.

Want to read sensor data? Connect sensors to another ESP32 or Arduino and send data to CloudMouse via WiFi or BLE. Want to control something? Send commands wirelessly. This approach keeps CloudMouse compact, clean, and truly wireless.

### Can I power CloudMouse with a battery?

Currently CloudMouse is designed for USB-C power only. Battery operation would require hardware modifications (adding battery management, power regulation, and a charging circuit). The ESP32-S3 with active display and LEDs draws significant current, so you'd need a decent-sized battery for reasonable runtime.

### What's the maximum WiFi range?

Typical indoor range is 30-50 meters depending on obstacles and interference. Outdoor line-of-sight can reach 100+ meters. The ESP32-S3 has good WiFi performance, but range depends heavily on your environment and the WiFi router/access point quality.

### Can CloudMouse work as a USB HID device?

Yes. The ESP32-S3 supports USB OTG and can act as a USB keyboard, mouse, or gamepad when connected via USB. Check the USB HID examples in the repository for ready-to-use code.

### How much power does CloudMouse consume?

Depends entirely on what you're running. With display on full brightness and all LEDs lit, expect around 500-800mA. With display dimmed and LEDs off, closer to 150-250mA. Deep sleep mode can reduce consumption to microamps, but you'll need to modify the firmware to use power-saving features.

## Software questions

### Can I use PlatformIO instead of Arduino IDE?

Yes, but we don't officially support it in the docs. If you're comfortable with PlatformIO, you can convert any Arduino sketch to a PlatformIO project. You'll need to configure the platform.ini properly for ESP32-S3 with the correct board settings. Check PlatformIO documentation for details.

### Can I use ESP-IDF instead of Arduino?

Yes, but again, no official documentation for it. ESP-IDF gives you more control and better performance but requires more advanced knowledge. If you're using ESP-IDF, you probably don't need our Getting Started guide. Just grab the pinout reference and go wild.

### What libraries do you recommend?

For display: LovyanGFX (best performance for ILI9488). For LEDs: FastLED (most features and effects). For encoder: ESP32Encoder or custom interrupt-based code. For WiFi/BLE: built-in ESP32 libraries work great. For web servers: ESPAsyncWebServer for better performance than default WebServer.

### How do I update the firmware wirelessly (OTA)?

ESP32 supports OTA updates. You need to include the ArduinoOTA library and set up OTA handling in your code. Check Arduino ESP32 OTA examples. Once configured, you can upload new firmware over WiFi without USB cable. Super useful for deployed devices.

### Can I run MicroPython or CircuitPython?

Technically yes, the ESP32-S3 supports MicroPython. However, none of our examples or boilerplate code are written for it, and you'd need to port all the display/LED/encoder code yourself. If you're a MicroPython expert, go for it. Otherwise, stick with Arduino/C++ for now.

## Development questions

### Where do I start if I'm new to embedded programming?

Start with the Getting Started guide to set up Arduino IDE. Then flash the Hello World boilerplate firmware to verify everything works. After that, pick the simplest example (LED Animations) and start modifying it. Change colors, timing, effects. Break it and fix it. That's the best way to learn.

### How do I debug my code?

Use Serial.println() everywhere. Print variable values, execution flow, error conditions. Open Serial Monitor and watch what's happening. For more advanced debugging, ESP32 supports JTAG debugging, but that requires additional hardware and setup. For 99% of projects, Serial debugging is enough.

### My code is too big and won't upload. What do I do?

First, make sure Flash Size is set to 16MB in Arduino IDE settings. If still too big, reduce image/font sizes, remove unused libraries, or move large data to SPIFFS/LittleFS filesystem. The ESP32-S3 has plenty of flash, so if you're hitting limits, something's probably misconfigured.

### Can I use the two CPU cores separately?

Yes. The ESP32-S3 has dual cores that can run tasks independently. Use FreeRTOS tasks (xTaskCreatePinnedToCore) to assign specific tasks to specific cores. Typical pattern: networking on Core 0, UI rendering on Core 1. Check the SDK firmware for an example of dual-core architecture.

## Community questions

### Where can I get help?

Discord for quick questions and real-time chat. GitHub Issues for bug reports and feature requests. Community forum for in-depth discussions and project showcases. Choose based on your need: quick answer (Discord), bug report (GitHub), long discussion (forum).

### Can I contribute to the project?

Please do! We need examples, documentation improvements, bug fixes, library updates, design improvements. Fork the repo, make your changes, submit a pull request. All contributions are welcome. Even fixing typos in documentation helps.

### Where can I share my CloudMouse projects?

Post on Discord, share on the forum, tweet with #CloudMouse hashtag, add to GitHub discussions. We love seeing what people build. Best projects get featured on our website and social media.

## Purchasing questions

### Where can I buy CloudMouse?

Check the official CloudMouse website for current availability and authorized distributors. We also occasionally run limited production batches. Join the Discord or follow on Twitter for announcements.

### Do you ship internationally?

Yes, we ship worldwide. Shipping costs and times vary by location. Check the website for specific details for your country.

### What's included in the box?

CloudMouse device with Asteroids pre-loaded, USB-C cable, quick start guide. Everything you need to get started. No additional components required.

## Still have questions?

Ask on Discord, post on the forum, or open a discussion on GitHub. The community is friendly and helpful. Don't be shy.