<h1 align="center">MakerGear M2 (Rev.C+) Marlin 2.1.2 Firmware Beta</h1>
<h4 align="center">Coming soon</h4>

Each branch of this GitHub repository will include a different, pre-built M2 hardware configuration, removing the need to use Arduino. Hopefully this combined with a new firmware selector and documentation will streamline the firmware uploading process!

## New Marlin 2.1.x+ Features:

- Nozzle Park (on pause)
- Babystepping
- Advance Pause (M600 GCode)
- LCD Features:
  - Starting Height Calibration Menu
  - Extrude Menu
  - Babystepping Menu
  - Advanced Pause Menu

## Installing Marlin 

There is a firmware .hex file within the /Firmware/Builds/ directory of each firmware branch. Users can download the .hex file for their machine's hardware configuration and then (easily!) upload the firmware to their M2 printer using PrusaSlicer over USB connection. For the time being I've (roughly) copied [Prusa's documentation](https://help.prusa3d.com/article/firmware-updating-mk3s-mk3s-mk3_2227) on how to upload firmware:

1. To flash the firmware into your printer, connect the RAMBo board to your computer using the square-shaped USB-B 2.0 cable. The printer must be ON!
2. Download firmware
3. Open PrusaSlicer, click on the 'Configuration' menu, and select 'Flash printer firmware'
4. Click on the Browse button and choose the .hex file
5. Click Flash! and let the procedure complete

## Notes: 

- There are thirty-two supported hardware configurations
- I'm unable to support the (~2015) v3B hotend, 12/19v power supply, or the Viki LCD
- Linear Advance is disabled by default because it would need to be manually configured for each filament material type
  -  If you'd like to enable this feature you configure it manually

## Manually Editing/Building Marlin 2.1

To build and upload Marlin you will use one of these tools:

- The free [Visual Studio Code](https://code.visualstudio.com/download) using the [Auto Build Marlin](https://marlinfw.org/docs/basics/auto_build_marlin.html) extension.
- The free [Arduino IDE](https://www.arduino.cc/en/main/software) : See [Building Marlin with Arduino](https://marlinfw.org/docs/basics/install_arduino.html)

Marlin is optimized to build with the **PlatformIO IDE** extension for **Visual Studio Code**. You can still build Marlin with **Arduino IDE**, and we hope to improve the Arduino build experience, but at this time PlatformIO is the better choice.

## GitHub Workflow to Automate Building Firmware

I customized the GitHub workflow from [tinuva/b1seplus-marlin-build](https://github.com/tinuva/b1seplus-marlin-build), in order to build Marlin .hex files automatically. Thank you [tinuva](https://github.com/tinuva) and [frealmyr](https://github.com/frealmyr) for making this possible!
