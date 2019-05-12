---
layout: project
title: Pulsing LED
description: Shows how to apply special effects on the LED connected to the snap:bit. The micro:bit automatically changes the brightness of the LED in a way to simulate a smoothly pulsing LED.
category: project
slug: pulsing-led
diagram: led
makecode: _JHU45o3md3yA
requires: B1,S1,D1,1,3x3
---

This project builds on top of what we learned in the [Blinking LED](blinking-led.html) and the [Adjust LED brightness](adjust-led-brightness.html) projects.

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers and the micro:bit displays the snap:bit logo. It also sets the brightness level to 0 and the increment step to 1.

When the "on start" event finishes, the "forever" loop starts. It changes the brightness level by the increment step. In the beginning, the increment step is 1, which means that the brightness will increase with one level. Then it writes an analog signal to pin P1, calculated using the 2<sup>n</sup> - 1 formula, where _n_ is the current brightness level (see the [Adjust LED brightness](adjust-led-brightness.html) projects for details). This changes the current flow between the P1 and GND pins. The LED changes its brightness based on how much current flows. The loop now pauses shortly for 50 milliseconds.

Next, the "forever" loop checks if the current brightness level reached a maximum of 10. In such case, it changes the increment step to -1, which starts decreasing the current brightness with one level on each iteration of the "forever" loop. When the current brightness level drops down to 0, the increment step changes back to 1. In addition, the loop pauses for half a second (500 ms) for a better pulsing effect.

The "forever" loop executes the instructions in its body again and again until the micro:bit is turned off. So does the pulsing.

Try experimenting by changing the duration of the pause after the "analog write" instruction. How does the pulsing change if you set the pause to:
- 10 ms
- 200 ms?