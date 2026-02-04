# Serial-Communication-and-Firmware-Extraction
This repo is a series of tutorials to help develop skills with:
* Serial communication (UART) using both hardware and software serial
* Using TTL serial adapters/cables with microcontrollers
* Comparing hardware/firmware/software behaviors across interfaces
* Getting comfortable with firmware formats (and later, extraction workflows)

## Table of Contents
* [Project 1: Interfacing with Serial](#project-1-interfacing-with-serial)
* [Background](#background)
* [Requirements](#requirements)
* [Procedure](#procedure)
* [Results/Discussion](#results/discussion)
* [Project 2: Programming Arduino with TTL Cable](#project-2-programming-arduino-with-ttl-cable)
* [References](#references)

## Project 1: Interfacing with Serial
### Background
This project aims to access and read two separate serial data streams from an Arduino Uno. One through the normal USB programming connection, and one through a  USB-to-TTL (UART) adapter. 
#### Hardware Serial
Hardware serial is a physical UART component built into the microcontroller.  
* On an Arduino Uno, this is typically the UART tied to pins **0 (RX)** and **1 (TX)**.
* It’s typically more reliable and accurate (timing handled by hardware).

[https://www.tutorialspoint.com/difference-between-hardware-serial-and-software-serial-in-arduino] 

#### Software Serial
Software serial emulates UART behavior in software on “regular” GPIO pins.  
* Works when you need another serial channel. Multiple software serial ports are possible
* Tradeoffs: More CPU overhead and more sensitive to timing, baud rate, and interrupts.

[https://www.tutorialspoint.com/difference-between-hardware-serial-and-software-serial-in-arduino]
[https://www.tutorialspoint.com/software-serial-in-arduino]

#### TTL Cable (USB-to-TTL Serial Adapter)
A TTL cable/adapter converts USB to logic-level serial(TX/RX/GND).  

[https://learn.sparkfun.com/tutorials/logic-levels/ttl-logic-levels#:~:text=TTL%20is%20an%20acronym%20for,threshold%20voltage%20levels%20to%20know] 

### Requirements 
#### Materials 
* Arduino Uno Board
* USB-B Data Cable
* USB-to-TTL serial adapter/cable
* Laptop/Desktop 
#### Software
* Arduino IDE

### Procedure
1. Flash "serialMonitorTest.ino" onto an Arduino Uno.
2. Connect the Arduino to your laptop/desktop:
   * USB Cable (Hardware Serial)
   * TTL Adapter to pins 2/3 (RX/TX) and GND
4. Open two sketches (different ports) and stream serial in both sketches.

### Results/Discussion 
Both serial monitors display continuous output, and I am able to confirm that: 
* Hardware Serial is streaming over USB, and
* Software Serial is streaming over the TTL adapter.

This demonstrates how multiple serial data streams can be handled on a single microcontroller.

## Project 2: Programming Arduino with TTL Cable 

