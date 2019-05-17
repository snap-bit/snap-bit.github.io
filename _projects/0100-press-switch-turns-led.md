---
layout: project
title: Turn LED on and off using the press switch (S2)
description: Shows how to control the state of the LED with the press switch. Pressing the switch once turns the LED on. Pressing the switch again turns the LED off.
category: project
slug: press-switch-turns-led 
diagram: led-press
makecode: _K8eWE6JVPRUr
requires: B1,S1,S2,D1,1,3x3
---

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers and the micro:bit displays the snap:bit logo. 

Press the press switch (S2) and release it within 1 second. This closes the circuit between the P2 and GND pins of the micro:bit. The “on pin P2 pressed” event triggers and the micro:bit writes a digital 1 signal to pin P1. This closes the circuit between the P1 and GND pins and the LED (D1) turns on. Press and release the press switch once again. The "on pin P2 pressed" event triggers once again. This time the micro:bit writes a digital 0 signal to pin P1. This opens the circuit between the P1 and GND pins and the LED turns off.

Note that the code uses a helper variable with name “on”. When the micro:bit writes a digital 1 signal to pin P1, it sets “on” to 1. When the micro:bit writes a digital signal 0 to pin P1, it sets “on” to 0. The value of the “on” variable is checked every time the “on pin P2 pressed” event triggers. This helps the micro:bit alternate writing digital 0 and 1 signals to pin P1 every time the press switch (S2) is pressed.