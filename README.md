# Detect a Knock (Arduino Project)

**Author:** [mobinyousefi-cs](https://github.com/mobinyousefi-cs)\
**License:** MIT

## Overview

This project demonstrates how to use a **Piezo element** to detect
vibrations such as knocking on a door, table, or any solid surface.

A piezo generates voltage when physically deformed by vibration, sound
waves, or mechanical strain. This property allows it to be used both for
**tone generation** and **vibration sensing**.

In this project, the Arduino reads the piezo signal through the
`analogRead()` function. The board converts the input voltage (0--5V)
into a 10‑bit value (0--1023) using the **ADC** (Analog‑to‑Digital
Converter). If the reading exceeds a defined threshold, the Arduino
sends the string **"Knock!"** over the Serial Monitor.

## Features

-   Detects vibration through a piezo sensor\
-   Sends a serial message when knocking is detected\
-   Demonstrates analog input reading and basic signal thresholding\
-   Fully open‑source (MIT License)

## How It Works

1.  The piezo is connected to **Analog Pin 0**.\
2.  A **1 MΩ resistor** is placed in parallel with the piezo to reduce
    voltage spikes and protect the analog input pin.\
3.  When a knock occurs, the piezo generates a voltage spike.\
4.  Arduino reads this spike; if it exceeds the threshold, it prints
    **"Knock!"** to the Serial Monitor.

## Circuit Description

Piezos are polarized:\
- **Red wire → Analog Pin 0**\
- **Black wire → GND**

A **1 MΩ resistor** is used in parallel to limit current and ensure safe
operation.

Bare piezo discs (metal discs) work well as sensors and perform best
when pressed, taped, or glued firmly to the sensing surface.

## Schematic Summary

-   Piezo connected to **A0**\
-   1 MΩ resistor placed between the piezo leads\
-   Resistor protects the analog input from excessive current

## Getting Started

1.  Connect the circuit as described above.\
2.  Upload the sketch to your Arduino board.\
3.  Open the Serial Monitor at **9600 baud**.\
4.  Knock on the surface where the piezo is attached.\
5.  Observe the **"Knock!"** messages.

## License

This project is distributed under the **MIT License**.\
See the `LICENSE` file for more details.

------------------------------------------------------------------------

Happy tinkering and enjoy detecting knocks with Arduino!
