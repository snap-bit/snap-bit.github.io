---
layout: project
title: Connect photoresistor to snap:bit
description: Shows how to connect the photoresistor to snap:bit and use it as a light sensor input for the micro:bit.
category: lesson
slug: connect-photoresistor
diagram: photoresistor
makecode: _H4e6yk5jXKkX
requires: B1,S1,RP,1,2,2x3
---

The photoresistor (RP) is a special resistor that can be used as a light sensor. Its resistance value changes from nearly infinite in total darkness to about 1 KΩ when bright light shines directly on it.

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The "forever" loop starts, reads the analog input from pin P2 and sets the value to the "light" variable. Then it displays the value from the "light" variable on the micro:bit display by plotting a vertical bar. If the value is "0", only the bottom middle LED on the display is alight. If the maximum value of "1023" is read from pin P2 then all of the LEDs are alight. This process repeats endlessly in the "forever" loop and the vertical bar on the display is adjusted in real-time as the light shining on the photoresistor changes.

If you run this project during the day, there should be a lot of light shining on the photoresistor. Its resistance value would be low and the micro:bit would read a value closer to "0" from pin P2.

Cover the photoresistor with your hand and see more LEDs alight on the micro:bit display. This happens because the resistance value of photoresistor increases due to the less light shining on it. The higher resistance causes the micro:bit to read a higher analog value from pin P2.

Can you go to a darker place? Check how the micro:bit will detect the change in the ambient light.