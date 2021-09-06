# CircuitPython

# Board

LilyGo

V1.1

ESP32_S2_WOOR

Chip ESP32-S2-WROOM


# Found Comments about Board

It is working. Esptool v.3 is needed to flash. I can't find MicroPython for this model, but CircuitPython with OTG mode can be used (for NanoESP32 S2 or Saola 1 w/WROOM). Delivered in month.


https://github.com/platformio/platform-espressif32/issues/349



# Installing

https://circuitpython.readthedocs.io/en/latest/ports/esp32s2/README.html


https://circuitpython.org/board/lilygo_ttgo_t8_s2_st7789/


# Installing Python 3.7

sudo add-apt-repository ppa:deadsnakes/ppa

sudo apt-get update

sudo apt-get install python3.7

python3.7 -m pip install pip

~/Documents/Code/env-mu/bin/python -m pip install --upgrade pip

sudo apt-get install python3.7-venv

python3.7 -m venv mu-venv

source mu-venv/bin/activate

python -m pip install mu-editor

python -m mu

# Flashing to ESP32S2

Command suggested  esptool.py –chip esp32s2 –port (COMPORT) –baud 115200 write_flash 0x000 “adafruit-circuitpython-lilygo_ttgo_t8_s2_st7789-xx_XX-6.2.0.bin”

Command worked esptool.py write_flash 0x000 “adafruit-circuitpython-lilygo_ttgo_t8_s2_st7789-xx_XX-6.2.0.bin”

Output during Flashing

esptool.py write_flash 0x000 "adafruit-circuitpython-lilygo_ttgo_t8_s2_st7789-en_GB-6.3.0.bin"
esptool.py v3.1
Found 1 serial ports
Serial port /dev/ttyUSB0
Connecting........_
Detecting chip type... ESP32-S2
Chip is ESP32-S2
Features: WiFi, ADC and temperature sensor calibration in BLK2 of efuse
Crystal is 40MHz
MAC: 7c:df:a1:0d:f7:86
Uploading stub...
Running stub...
Stub running...
Configuring flash size...
Flash will be erased from 0x00000000 to 0x0014dfff...
Compressed 1367600 bytes to 866339...
Wrote 1367600 bytes (866339 compressed) at 0x00000000 in 76.6 seconds (effective 142.8 kbit/s)...
Hash of data verified.

Leaving...
(env-mu) andrewcgaitskell@andrewcgaitskell-ubuntu:~/Downloads$ python -m mu
Logging to /home/andrewcgaitskell/.cache/mu/log/mu.log
(env-mu) andrewcgaitskell@andrewcgaitskell-ubuntu:~/Downloads$ python -m mu
Logging to /home/andrewcgaitskell/.cache/mu/log/mu.log

python -m pip install --upgrade --force-reinstall adafruit-blinka Adafruit-PlatformDetect


