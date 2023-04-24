# CircuitPython RP2040 Projects using Adafruit's HID Library

This project is based on the following GitHub Repo:

https://github.com/dbisu/pico-ducky

The payload was created by SurfKahuna (RJC)

The payload targets Windows computers. First it opens up Notepad using Run and draws Bart Simpson in ASCII characters then writes the message: "I will learn to lock my computer." several times before locking the computer.

## Steps:

  - Download the latest [CircuitPython](https://circuitpython.org/board/raspberry_pi_pico/) firmware and the [Adafruit HID library](https://github.com/adafruit/Adafruit_CircuitPython_HID/releases), you should have a `.UF2` file and a `.ZIP` file.
  - Connect the Raspberry Pi Pico (RP2040) to computer using USB-A to Micro-USB cable.
  - Put the Pico into bootloader mode by holding down the BOOTSEL button when plugging in the USB.
  - The Pico should appear as a mass storage device.
  - Move the `.UF2` firmware file that was downloaded from Circuit Python's [website](https://circuitpython.org/board/raspberry_pi_pico/).
  - The Pico should now appear as `CIRCUITPY`
  - Extract the contents of the `.ZIP` file that was downloaded from [Adafruit HID library](https://github.com/adafruit/Adafruit_CircuitPython_HID/releases) and  search for the following folder:
    - `adafruit_hid`
  - Select `adafruit_hid` and copy it into the `lib` folder in `CIRCUITPY`
  - To make a copy of this project you can overwritte the contents of the `payload.dd` and `code.py` file with the code from this repo. Just be forewarned as the code will automatically run upon plugging in the Pico. [`code.py`](https://github.com/dbisu/pico-ducky/blob/main/duckyinpython.py) is a Python script that converts DuckScript into MicroPython code for Pico. The `payload.dd` file is a binary file that contains the keystrokes and other actions that will be executed by the Pico when it is plugged in.
