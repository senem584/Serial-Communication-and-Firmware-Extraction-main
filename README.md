# Serial-Communication-and-Firmware-Extraction
This repo is a series of tutorials to help develop skills with:
* Serial communication (UART) using both hardware and software serial
* Using TTL serial adapters/cables with microcontrollers
* Comparing hardware/firmware/software behaviors across interfaces
* Getting comfortable with firmware formats (and later, extraction workflows)

## Table of Contents
* [Project 1: Interfacing with Serial](#project-1-interfacing-with-serial)
* [Project 2: Programming Arduino with TTL Cable](#project-2-programming-arduino-with-ttl-cable)
* [Project 3: Arduino as programmer/debug board with Arduino ISP](#project-3-arduino-as-programmerdebug-board-with-arduino-isp)

## Project 1: Interfacing with Serial
### Background
#### Hardware Serial
**Hardware serial** is a physical UART peripheral built into the microcontroller.  
* On an Uno, this is typically the UART tied to pins **0 (RX)** and **1 (TX)**.
* It’s generally more reliable and accurate (timing handled by hardware).
[https://www.tutorialspoint.com/difference-between-hardware-serial-and-software-serial-in-arduino] 

#### Software Serial
**Software serial** emulates UART behavior in software on “regular” GPIO pins.  
* Works when you need *another* serial channel. Multiple software serial ports are possible
* Tradeoffs: more CPU overhead and more sensitive to timing, baud rate, and interrupts.
[https://www.tutorialspoint.com/difference-between-hardware-serial-and-software-serial-in-arduino]
[https://www.tutorialspoint.com/software-serial-in-arduino]

#### TTL Cable (USB-to-TTL Serial Adapter)
A **TTL cable/adapter** converts USB on your computer to **logic-level serial** (TX/RX/GND).  
Common chips: FTDI, CP210x, CH340, etc.

### Requirements 
#### Materials 
* Arduino Uno Board
* USB-B Data Cable
* TTL Cable
* Laptop/Desktop with Arduino IDE

#### Software
* Arduino IDE
* Python 3
* `pyserial` (recommended)

### Resources

## Project 2: Programming Arduino with TTL Cable

## Project 3: Arduino as programmer/debug board with Arduino ISP 
