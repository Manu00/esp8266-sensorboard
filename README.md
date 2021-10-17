# esp8266-sensorboard
With this small project i make my first steps into prototyping and pcb-design, using the esp8266.

# Goals
I'm trying to build small easy to use and flexible boards that will primarily be used to measure temperature. Thanks to five exposed GPIO pins many things can be connected to it and one can even use a battery management board to use it wirelessly too. Also the exposed RX/TX pins and buttons make it easy to program which was very important to me. 

# Getting started
After getting everything from the "shopping list" I soldered it to the pcb. 
1. Get everything from the "shopping list" and the PCBs
2. Most components are easy to place but watch out for the resistors and capacitors, R1, R2, R3 are 10kOHM and R4 is a 1kOHM resistor. 
3. I found the best way to solder SMDs is to place some solder one one pad of the pcb then place the resistor/button/.. heat it so it flows in place and then solder the other side (Beware the AMS1117 is difficult to solder because this solder connection dissipates heat very well)
### Flashing
You can use many tools to flash an esp8266 but the best one is still [esptool.py](https://github.com/espressif/esptool)
1. Connect your usb-to-serial converter (3.3v!!) to the device but not the PC
2. Press and hold the PRG-Button while connecting it to the PC
3. Release the button and flash your firmware

# Usage
While I run [Home Assistant](https://www.home-assistant.io/) which has a great integration with [espHome](https://esphome.io/) you don't have to use this, [Tasmota](https://tasmota.github.io/docs/) is a great alternative or you can write your own code with platformIO or ArduinoIDE it's an completely open device

## Shopping List
- resistor 10k 3x
- resistor 1k 1x
- button 2x
- micro usb female 1x
- ams1117 3v3 1x
- esp12F 1x
- capacitor 100uF 1x
- capacitor 10uF 1x

Optional:
- BME/P 280 1x

## Images
![pcb](https://raw.githubusercontent.com/Manu00/esp8266-sensorboard/main/images/pcb_v0.1.svg?sanitize=true)
![schematic](https://raw.githubusercontent.com/Manu00/esp8266-sensorboard/main/images/schematic.svg?sanitize=true)

### PCBs arrived
![schematic](https://raw.githubusercontent.com/Manu00/esp8266-sensorboard/main/images/board-without.jpg?sanitize=true)
raw pcb without components
<br/>
<br/>
![schematic](https://raw.githubusercontent.com/Manu00/esp8266-sensorboard/main/images/board-with.jpg?sanitize=true)
sadly the capacitors didn't arrive at time but i can still use it with 3.3v
