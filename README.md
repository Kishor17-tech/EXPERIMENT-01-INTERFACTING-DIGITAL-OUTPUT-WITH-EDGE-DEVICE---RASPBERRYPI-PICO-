# EXPERIMENT-01-INTERFACTING-DIGITAL-OUTPUT-WITH-EDGE-DEVICE---(RASPBERRYPI-PICO)
### NAME K R KISHOR
### DEPARTMENT CSE(IOT)
### ROLL NO 212224110032
### DATE OF EXPERIMENT 24/05/2025

### AIM
To interface a digital output device (LED) with the Raspberry Pi Pico and control it using MicroPython.

## APPARATUS REQUIRED:
Raspberry Pi Pico
LED (Light Emitting Diode)
330Ω Resistor
Breadboard
Jumper Wires
USB Cable
 ## THEORY:

 ![image](https://github.com/user-attachments/assets/abeabf63-f321-471e-a991-3adaa9043a8b)

 
 
 
 
 ### FIGURE-01 RASPI PICO PINOUT DIAGRAM:



 Raspberry Pi Pico is a microcontroller board based on the RP2040 chip. It supports MicroPython, making it suitable for IoT and embedded applications.
The Raspberry Pi Pico is a compact microcontroller board featuring a 40-pin layout, including power, ground, GPIO, and communication interface pins. It operates with a dual-core ARM Cortex-M0+ processor and supports MicroPython and C/C++ programming. The power pins include VBUS (5V from USB), VSYS (1.8V to 5.5V input), 3V3(OUT) (regulated 3.3V output), and multiple ground (GND) connections. The board offers 26 multi-purpose GPIO pins (GP0 to GP28), which can be used for digital input, output, PWM, and communication interfaces such as I2C, SPI, and UART. It also features three analog-to-digital converter (ADC) pins (GP26, GP27, GP28), used for reading analog sensor values, along with an ADC_VREF pin to set the reference voltage. For communication, I2C (SDA, SCL), SPI (MOSI, MISO, SCK), and UART (TX, RX) interfaces are mapped across different GPIO pins, allowing seamless connectivity with sensors and peripherals. All GPIO pins support PWM (Pulse Width Modulation), making it useful for motor control, LED brightness adjustment, and sound applications. The BOOTSEL button enables USB mass storage mode for firmware flashing, while the DEBUG pins (SWD interface) provide debugging capabilities. With its low power consumption, flexible GPIO options, and rich interface support, the Raspberry Pi Pico is widely used for IoT, embedded systems, robotics, and automation projects.


## Working Principle:

The LED is connected to one of the GPIO pins of the Pico.
The MicroPython script sets the GPIO pin HIGH to turn the LED ON and LOW to turn it OFF.
CIRCUIT DIAGRAM
Connect the anode (longer leg) of the LED to GP15 via a 330Ω resistor.
Connect the cathode (shorter leg) of the LED to GND (ground).


## PROGRAM (MicroPython):
```
## PROGRAM 1:
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
while True:
    led1.toggle()
    sleep(0.5)

## PROGRAM 2:
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
led2=Pin(1,Pin.OUT)
led3=Pin(2,Pin.OUT)
while True:
    led1.toggle()
    sleep(0.5)
    led2.toggle()
    sleep(0.5)
    led3.toggle()
    sleep(0.5)

## PROGRAM 3:
from machine import Pin
from utime import sleep
led1=Pin(0,Pin.OUT)
led2=Pin(1,Pin.OUT)
led3=Pin(2,Pin.OUT)
buzz=Pin(3,Pin.OUT)
while True:
    led1.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)
    led2.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)
    led3.toggle()
    sleep(0.5)
    buzz.toggle()
    sleep(0.5)


 



 
````

### OUTPUT:  


# FIGURE -01 ADD TITILE HERE 
![Screenshot 2025-02-24 114244](https://github.com/user-attachments/assets/b4a0fba2-ac2d-4f82-b201-da9de71cfc22)


#  FIGURE -02 ADD TITILE HERE
![Screenshot 2025-02-24 113807](https://github.com/user-attachments/assets/2df9ce91-7e24-44bb-aa75-dd514e9259eb)


# FIGURE -03 ADD TITLE HERE 
![Screenshot 2025-02-24 113557](https://github.com/user-attachments/assets/98957983-32e3-49cc-8ec6-29708e08e5ec)




 
## RESULTS:
The LED connected to the Raspberry Pi Pico successfully turns ON and OFF at  user defined time  confirming the proper interfacing of a digital output.
