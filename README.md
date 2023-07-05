# yardy_bot_spi_display

## Setup
- [Helpful link #1](https://learn.adafruit.com/adafruit-mini-pitft-135x240-color-tft-add-on-for-raspberry-pi/python-setup)
- [Helpful link #2](https://learn.adafruit.com/adafruit-mini-pitft-135x240-color-tft-add-on-for-raspberry-pi/1-3-240x240-kernel-module-install)
```
sudo pip3 install --upgrade adafruit-python-shell click
git clone https://github.com/adafruit/Raspberry-Pi-Installer-Scripts.git
cd Raspberry-Pi-Installer-Scripts
sudo python3 adafruit-pitft.py --display=st7789_240x240 --rotation=0 --install-type=console
pip3 install adafruit-circuitpython-rgb-display
pip3 install --upgrade --force-reinstall spidev
sudo apt-get install fonts-dejavu
sudo apt-get install python3-pil
sudo apt-get install python3-numpy
sudo apt-get install python3-dev python3-rpi.gpio
```

- Set the console output to the display
-- Add the following line to the end of `/boot/firmware/config.txt`:
    ```
    dtoverlay=spi1-3cs
    ```