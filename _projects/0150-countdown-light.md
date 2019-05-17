---
layout: project
title: Countdown light and sound
description: Use the press switch to increment the counter. Then press the A button on the micro:bit and watch how the counter automatically starts to count down with light and sound.
category: project
slug: countdown-light
diagram: countdown-light
makecode: _ALhaMqaHMKdt
requires: B1,S1,S2,D1,WC,1,2,3x3,4
featured: true
---

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers, which sets the "count" variable to 0 and displays it on the micro:bit.

Press the press switch (S2) and release it within 1 second. This closes the circuit between the P2 and GND pins of the micro:bit. The “on pin P2 pressed” event triggers, which increments the "count" variable by 1 and updates the display of the micro:bit with the new value. Press the switch as many time as you wish and watch how the counter increments.

Now press the A button on the micro:bit. The "on button A pressed" event triggers and the micro:bit writes a digital 1 signal to pin P1. This closes the circuit between the P1 and GND pins and the LED (D1) turns on. 

Then the micro:bit executes a loop as many times as the value of the "count" variable. In each iteration, the micro:bit plays a sound, then pauses for 1 second, decreases the value of the "count" variable by 1, and updates the display with the new value. When the value of the "count" variable is down to 0, the loop ends and the micro:bit plays the "dadadum" melody.

Finally, the micro:bit writes a digital 0 signal to pin 1. This opens the circuit between the P1 and GND pins and the LED turns off.