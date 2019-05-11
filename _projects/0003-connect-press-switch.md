---
layout: project
title: Connect press switch (S2) to snap:bit
description: Show how to receive input from the press switch and process it in the micro:bit.
category: lesson
slug: connect-press-switch
diagram: press-switch
makecode: _Fkx5gkDa7MWa
requires: B1,S1,S2,1,2,2x3
---

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers and the micro:bit displays the smiley face. Press the press switch (S2) and release it within 1 second. This closes the circuit between the P2 and GND pins of the micro:bit. The "on pin P2 pressed" event triggers and the micro:bit now displays a grumpy face. Press and release the press switch once again. The micro:bit displays the smiley face again.

Note that the code uses a hepler variable with name "smile". When the micro:bit displays the smiley face, it sets "smile" to 1. When the micro:bit displays the grumpy face, it sets "smile" to 0. The value of the "smile" variable is checked every time the "on pin P2 pressed" event triggers. This helps the micro:bit alternate the smiley and grumpy faces every time the press switch (S2) is pressed.

The press switch (S2) can be connected across any of the 0, 1 and 2 snaps and the GND snap. Pressing and releasing the press switch within 1 second triggers the events "on pin P0 pressed", "on pin P1 pressed" or "on pin P2 pressed" respectively.