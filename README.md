# In System MCU - A Platform for Arduino IDE

This Arduino Platform adds support for using Arduino IDE to set fuse bits and
upload sketches to ATmega microcontrollers that are in-system or on
a breadboard. Additionally no bootloader will be installed, allowing all of the
EEPROM to be used for the sketch.

Currently supported setups:

- ATmega328P using 16 MHz crystal
- ATmega328P using internal 8 MHz clock

Options are provided for setting the CKDIV8 clock division fuse.


## Installation with Boards Manager:

- Within Arduino IDE, open the Preferences window.
- In Additional Board Manager URLs, add
  http://www.bamfordresearch.com/files/package_jb23_insystemmcu_index.json
  and click ok.
- Open Tools > Board > Boards Manager...
- In the search box, start typing "in system".
- In System MCU will appear in the results, click Install.
- Arduino IDE automatically downloads this repository.
- New boards will appear under Tools > Board > In System MCU.

## Manual Installation

- Locate the hardware folder in your Sketchbook, eg. `~/Documents/Arduino/hardware/`
- Create a new folder inside it eg. `~/Documents/Arduino/hardware/In System MCU/`
- Copy the contents of this repository into the new folder.
- Restart Arduino IDE.
- New boards will appear under Tools > Board > In System MCU.


## Use

Connect in-system microcontroller to the programmer and select the correct
programmer under Tools > Programmer menu.

### Setting Fuse Bits and Removing Bootloader

Fuse Bits are used to set the microcontroller's clock source. Following this
procedure will also remove any bootloader and allow all of the microcontroller's
EEPROM to be used.

- Choose desired board eg. Tools > Board > ATmega328P 8 MHz (Internal)
- Select Tools > Burn Bootloader

### Uploading Sketch

- Make sure the same board is selected as was used to set fuse bits - this
  determines the expected clock speed during compilation.
- Select Sketch > Upload or click Upload in the toolbar - the programmer will be
  used automatically.


## More Information

Please visit http://www.bamfordresearch.com/arduino-platform
