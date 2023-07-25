# JBD BMS Serial MQTT Script
An Arduino script for the ESP-32 microcontroller that reads sends a received serial communication to a JBD BMS commonly used for DIY LiFPO4 batteries. This is base off of the script written by [playersz28](https://github.com/playersz28/JBD-ESP32) with changes to the MQTT schema.
I made a JST-PH jumper cable similar to the one used by the factory Bluetooth dongle to connect the circtuit board to the BMS serial communication port.
This is all made for communicating to an [MQTT client(https://github.com/michaelpappas/van_mqtt_client)] that managers other devices through a DIY camper van.

## Table of Contents
- [Wiring](#wiring)
- [Project Structure](#project-structure)
- [Further Improvements](#further-improvements)




### Wiring

The JST-PH connect has 12vdc ground, Tx, and Rx. An LM2596 dc-dc voltage converter is used to step the 12vdc (actually more like 13.5-14.4v) to 5vdc to power the ESP-32. The output of the LM2596 is connected to VIN and GND on the ESP. Tx and Rx from the JST are connected to TX2 and RX2, respectively.


## Project Structure

```
\                                   # project directory
 |--/images                         # project images
 |--boardHousing.3dm                # Board housing rhino file
 |--boardHousing.stl                # Board housing stl file
 |--BMS_HWSerial_to_MQTT_ESP32.ino  # arduino program for serial communication
 |--readme.md                       # project readme
```

## Further Improvements

1. Furthe document wiring and 3d printed case
2. Add switch on battery case to toggl power between ESP-32 and standard bluetooth dongle.










