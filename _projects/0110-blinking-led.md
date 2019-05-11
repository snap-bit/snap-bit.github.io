---
layout: project
title: Blinking LED
description: Shows how to turn the LED into a blinking LED. The micro:bit will automatically turn the LED on and off every second.
category: project
slug: blinking-led
diagram: led
makecode: _JwUWY6h5sg0e
requires: B1,S1,D1,1,3x3
featured: true
---

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers and the micro:bit displays the snap:bit logo.

At the same time the "forever" loop starts too. It first writes a digital 1 signal to pin P1. This closes the circuit between the P1 and GND pins and the LED (D1) turns on. Then it pauses for 1 second. Then it writes a digital 0 signal to pin P1. This opens the circuit between the P1 and GND pins and the LED turns off. The loop now pauses for another second. So far this made the LED be on for one second, and off for one second.

The "forever" loop executes the instructions in its body again and again until the micro:bit is turned off. Therefore, the LED will blink every second.

Try changing the duration of the pause instructions. For example:
- Change both to pause for 200 ms
- Change only the first pause to 200 ms and leave the other to pause for 1 second

How does this change the blinking of the LED?