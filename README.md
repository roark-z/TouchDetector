# TouchDetector
Python code to use the MPR121 capacitive touch sensor from Adafruit with a Raspberry Pi to count/log touches, while ignoring 'un-touch' events.
Counting/Logging times of touches happens in a threaded callback (using RPi.GPIO.add_event_callback) triggered from the IRQ pin on the MPR121. A custom callback can be installed which is run from the main callback. 

Adafruit_MPR121 requires the Adafuit MPR121 library which, in turn, requires CircuitPython and Adafruit Blinka for I2C-bus access:

sudo pip3 install --upgrade adafruit-python-shell
wget https://raw.githubusercontent.com/adafruit/Raspberry-Pi-Installer-Scripts/master/raspi-blinka.py
sudo python3 raspi-blinka.py
pip3 install adafruit-circuitpython-busdevice
pip3 install adafruit-circuitpython-mpr121

Updated 2022/10/17 to use new CircutPython-based adafruit libraries.
