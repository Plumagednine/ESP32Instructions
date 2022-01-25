# ESP32Instructions
**Adding Required ESP-32 Libraries**

Using ESP-32 Dev Boards, which are required if you want to use Bluetooth Serial to connect your gloves wirelessly, requires you to install additional packages to your Arduino IDE and a specific driver. Below is the procedure for doing so.

Most boards use the Silabs CP210x USB to UART chip, for which you have to install the driver:

1. Go to [Silicon Labs' official driver download page](https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers)
2. Go to the downloads section and download the "CP210x Windows Drivers" (fourth in the list).
3. Extract the .zip and run `CP210xVCPInstaller_x64.exe`.
4. Your ESP32 should now show up in your devices manager under ports as `Silicon Labs CP210x USB to UART Bridge (COM<number>)`. This is the port you should select in your IDE. If it doesn't show up, make sure you are using a data capable USB cable.

Adding the ESP32 package to your Arduino IDE:

1. Go to File > Preferences in your Arduino IDE
2. In the "Additional Board Manager URLs" field, enter this link: https://dl.espressif.com/dl/package_esp32_index.json and click the OK button
3. Go to Tools > Board > Boards Manager
4. Search "esp32" and install the "ESP32 by Espressif Systems" package.
5. Select your ESP32 board from Tools > Board  (Use ESP32 Dev Module if you are unsure) (I'm pretty sure we use either **NodeMCU-32S** or ESP32 Wrover Module)

**Adding ESP32Servo library for servo control**
1. Go to Tools > Manage Libraries in Arduino IDE
2. Search for ESP32Servo in the search bar
3. Find the ESP32Servo library authored by Kevin Harrington, click 'More info...' and then Install

![Alt text](https://content.instructables.com/ORIG/FOL/YWLI/JEOILQ5U/FOLYWLIJEOILQ5U.png?auto=webp&frame=1&width=1024&fit=bounds&md=a74a05c18f4b4d9f0db00ec63c7bc3c0)
