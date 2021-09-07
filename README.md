# CircuitPython

# PC Operating System

Ubuntu on Dual Boot with Windows

Ubuntu 20.04.2 LTS

# Board

LilyGo

V1.1

ESP32_S2_WOOR

Chip ESP32-S2-WROOM

# Circuit Python Download

Stupidly looked for LilyGo Circuit Python and wasted a few hours

Then tried WROOM version and all is well.

        saola_1_wroom-en_GB

https://circuitpython.org/board/espressif_saola_1_wroom/

# Found Comments about Board

It is working. Esptool v.3 is needed to flash. I can't find MicroPython for this model, but CircuitPython with OTG mode can be used (for NanoESP32 S2 or Saola 1 w/WROOM). Delivered in month.


https://github.com/platformio/platform-espressif32/issues/349


# Installing Python 3.7

My existing Python 3.8 did not support Mu, so needed to install previous version 3.7.


        sudo add-apt-repository ppa:deadsnakes/ppa

        sudo apt-get update

        sudo apt-get install python3.7

        python3.7 -m pip install pip

        ~/Documents/Code/env-mu/bin/python -m pip install --upgrade pip

        sudo apt-get install python3.7-venv

        python3.7 -m venv mu-env

        source mu-env/bin/activate

        python -m pip install mu-editor

        python -m mu

# Flashing to ESP32S2

## Command suggested

       esptool.py –chip esp32s2 –port (COMPORT) –baud 115200 write_flash 0x000 "adafruit-circuitpython-espressif_saola_1_wroom-en_GB-6.3.0.bin"

## Command worked

       esptool.py write_flash 0x000 "adafruit-circuitpython-espressif_saola_1_wroom-en_GB-6.3.0.bin"


# Once Flashed changed to OTG Mode

Toggle all DIP switches


