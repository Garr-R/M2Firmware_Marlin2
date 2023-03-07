<h1 align="center">MakerGear M2 (Marlin 2.1.2) Firmware Update</h1>
<h4 align="center">Coming soon</h4>

Each branch of this GitHub repository will include a different, pre-built M2 hardware configuration, removing the need to use Arduino. Hopefully this combined with a new firmware selector and documentation will simplify the firmware uploading process!

## New Marlin 2.1.x+ Features:

- Nozzle Park (on pause)
- Babystepping
- Advance Pause (M600 GCode)
- LCD Features:
  - Starting Height Calibration Menu
  - Extrude Menu
  - Babystepping Menu
  - Advanced Pause Menu

## Manually Building Marlin 2.1

There is a firmware .hex file within the /Firmware/Builds/ directory of each firmware branch. Users can download the .hex file for their machine's hardware configuration and then easily upload the firmware to their printer using the PrusaSlicer program over USB. Hopefully this combined with a new firmware selector and documentation will simplify the firmware process

Normally, to build Marlin firmware you would need to use either Arduino, or PlatformIO 

- The free [Visual Studio Code](https://code.visualstudio.com/download) using the [Auto Build Marlin](https://marlinfw.org/docs/basics/auto_build_marlin.html) extension.
- The free [Arduino IDE](https://www.arduino.cc/en/main/software) : See [Building Marlin with Arduino](https://marlinfw.org/docs/basics/install_arduino.html)

Marlin is optimized to build with the **PlatformIO IDE** extension for **Visual Studio Code**. You can still build Marlin with **Arduino IDE**, and we hope to improve the Arduino build experience, but at this time PlatformIO is the better choice.
