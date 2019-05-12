---
layout: project
title: Power micro:bit using the battery holder (B1)
description: Shows how to power the micro:bit from the battery holder of Snap Circuits.
category: lesson
slug: power-microbit
diagram: power-microbit
makecode: _VRz5UYA7MW4P
requires: B1,S1,3
---

The snap:bit has two special snaps -- 3V and GND, which are connected to the 3V and GND pins of the micro:bit respectively. If the micro:bit is not being powered by USB or its own battery, then the 3V pin can be used as a power input to power the micro:bit. 

When you close the slide switch (S1), current flows from the battery (B1) through the switch, the 3V pin of the micro:bit and the micro:bit board itself, then back to the battery through the GND pin of the micro:bit. This will power the micro:bit on and it will display the snap:bit logo. When the slide switch is opened, the current can no longer flow back to the battery, so the micro:bit switches off.

Powering the micro:bit this way is very convenient as you don't need to connect additional cables to the micro:bit to power it on. Using the slide switch (S1) to power the micro:bit on and off is also very useful. We will use this way of powering the micro:bit in most of the projects.

**Important!** Never connect a battery to the 3V snap of the snap:bit while powering the micro:bit using a USB cable or its own battery at the same time. This may damage the micro:bit, the snap:bit and other circuit components.

**Important!** Never apply more than 3V voltage to the 3V snap of the snap:bit. This may damage the micro:bit, the snap:bit and other circuit components. To be on the safe side always use the battery holder (B1). Be careful when using the Solar Cell (B2). Be sure to use it only under normal lighting, but not under very intense and bright light. You can also use Snap Module for AC Adapter (B6), but only connecting to the 3V snap. Never connect the 5V/6V snap to the 3V snap of the snap:bit. Never use any other power sources like the Battery Holder 4.5V (B3), the Rechargeable Battery 3.6V (B4), the 9V Holder (B5), or the Solar Cell (B7).