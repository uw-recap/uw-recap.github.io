---
layout: post
title:  "Time to Integrate"
date:   2019-02-20 17:00:00 -0500
categories: RECAP system-integration progress
---
In the past month we've been busy verifying the individual components of our prototype design. Here's a short overview of what those components are and what progress has been made.

## Enclosure
We're working on designing a 3D-printable version of the enclosure for the RECAP system. The main goal of the enclosure is to be mountable inside a vehicle without much difficulty.

## Hardware
RECAP has four major hardware components:

### Adafruit Feather M0 with RFM95 LoRa Radio
[This small chip](https://www.adafruit.com/product/3178), designed by Adafruit, contains both the brains of RECAP and the radio it uses for communication with other RECAP units. Its Cortex M0+ processor is quite powerful for an embedded device, and the RFM95 LoRa radio provides communication within a 1 km radius. Furthermore, the chip's footprint is compatible with any Featherwing device from Adafruit.

### Adafruit Ultimate GPS Featherwing
Speaking of compatibility with any Adafruit Featherwing, the [Ultimate GPS Featherwing](https://www.adafruit.com/product/3133) provides relatively accurate GPS data. It connects to the main processor via UART.

### Adafruit 3.5" TFT Featherwing
The [3.5" TFT Featherwing](https://www.adafruit.com/product/3651) is a 480x320 pixel LCD screen with a built-in graphics driver. It can be easily connected to via SPI, and the extra graphics driver takes a huge processing load off the Cortex M0+, allowing it to perform the computations required to make RECAP work.

### Freematics OBD-II UART Adapter
The [OBD-II UART Adapter v1](https://freematics.com/store/index.php?route=product/product&product_id=30), from Freematics, provides a simple UART interface between the vehicle's On-Board Diagnostics (OBD-II) and the main processor.

So far, we've made sure that all these components are functional and that they can each perform their tasks individually. Let's talk about some of the software we wrote to get things working.

## Software
The pieces of code that we've written so far are as follows:

### OBD-II and GPS Verification Code
We've been able to have a Feather gather both GPS and OBD-II data at the same time, and transmit it to another Feather using both the radio and a wired Serial connection. This will come in handy when testing our proof-of-concept.

### Data Filtering Algorithm
A basic implementation of the data filtering algorithm, which determines which vehicles are relevant to find the risk of collision, has been written. It'll be optimized when we put it together with the rest of the system components.

### LCD Benchmarking Code
Some methods to optimize the UI drawing were implemented and benchmarked to see how fast they would run. They may also need to be optimized further, depending on how things go during system integration.

## Next Steps
As you've probably guessed by now, our next step is to put all the things we've been working on together. We expect to be troubleshooting the system integration during the next week. Afterwards, it'll be time for testing our proof-of-concept, both in a simulated environment, and in an actual vehicle.

We'll keep you posted about our progress!
