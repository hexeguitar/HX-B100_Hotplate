# HX-B100_Hotplate
### Reverse engineered HP-B100 PCB hotplate + new controller design  
This project is aiming at creating a new more feature full cotnroller board for the Itech HP-B100 hot plate.  
First step is reverse engineering the original hardware. All files (KiCad7 project, pictures) are placed in the **HP-B100_OriginalHardware** folder.  
The controller is built around:
- ATMEGA88P MCU
- TM7711 used as thermocouple ADC
- TM1638 used to drive LED displays and LEDs #
- BTA16-800 triac switched with MOC3041M as main power switch element
- small 3VA 12VAC transformer powering the 5VDC supply.  
  
The original board is already a very nice base for further development. Big thumbs up for the designer!  
Conveniently what we have there is:
- full PORTD + GND available as pin header
- two segments (-2 outputs used for status LEDs) of the LED driver avaialble for use
- the main mcu is pin to pin compatible with ATMEGA328P in case more Flash space is needed.
- AVR ISP header available for easy programming.
--- 

The plan is to create a new board with a few mode extras:  
- replace 7 segment LED displays with SPI TFT ones and create a more modern UI
- add two small fans for cooling the hotplate
- add reflow profile feature and presets for reflow, pre-heating etc.
  
Work in progress...

--- 
03.2023 Piotr Zapart  
www.hexefx.com