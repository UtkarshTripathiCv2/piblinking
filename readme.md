login as: jackalkirpi
password: (your password)
jackalkirpi@jacks:~ $
gpio -v
sudo apt install python3-rpi.gpio -y
nano led.py
import RPi.GPIO as GPIO
import time

GPIO.setmode(GPIO.BCM)
GPIO.setup(17, GPIO.OUT)

while True:
    GPIO.output(17, True)
    time.sleep(1)
    GPIO.output(17, False)
    time.sleep(1)
python3 led.py
CTRL + C


# Raspberry Pi 4 - LED Blinking Project

## 📌 Project Description
This project blinks an LED using Raspberry Pi GPIO17 with Python.

It turns ON for 1 second and OFF for 1 second continuously.

---

## 🛠 Requirements
- Raspberry Pi 4
- 1 LED
- 1 Resistor (220Ω or 330Ω)
- Breadboard
- Jumper wires

---

## 🔌 Connections

| Component | Connect To |
|------------|------------|
| LED Long Leg (+) | GPIO17 (Pin 11) |
| LED Short Leg (-) | Resistor |
| Resistor | GND (Pin 6) |

GPIO Mode used: BCM

---

## 📝 Python Code (led.py)

```python
import RPi.GPIO as GPIO
import time

GPIO.setmode(GPIO.BCM)
GPIO.setup(17, GPIO.OUT)

while True:
    GPIO.output(17, True)
    time.sleep(1)
    GPIO.output(17, False)
    time.sleep(1)
python3 led.py
CTRL + C
