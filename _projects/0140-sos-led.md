---
layout: project
title: SOS LED
description: Shows how to turn the connected LED into a Morse code emitter by programming the micro:bit for sending the SOS emergency signal.
category: project
slug: sos-led
diagram: led
makecode: _0KJeC4XJY5RU
requires: B1,S1,D1,1,3x3
---

The [Morse code](https://en.wikipedia.org/wiki/Morse_code) is a scheme for encoding text as a sequence of _dots_ and _dashes_.

![Morse Code](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/International_Morse_Code.svg/315px-International_Morse_Code.svg.png)

Morse code can be transmitted in various ways, including radio waves, sound waves, visual light, etc.

This project programs the micro:bit to send the [SOS](https://en.wikipedia.org/wiki/SOS) signal using the connected LED. The LED has to emit 3 short light signals, then 3 long light signals, then 3 short light signals again.

We define two functions: "dot" and "dash". The "dot" function writes a digital 1 signal to pin P1 to turn the LED on. Then the function pauses for "unit" milliseconds, where "unit" is a variable that defines the time unit for the Morse code. Then the "dot" function writes a digital 0 signal to pin P1 to turn the LED off. Then it pauses again for "unit" ms.

Executing the "dot" function results in a short light emitted from the LED and a short pause with the LED off. This is equivalent to emitting the _dot_ of the Morse code.

The "dash" function is very similar to the "dot" function. The difference is that that the LED is on for 3 times the "unit" duration. This is equivalent to emitting the _dash_ of the Morse code.

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers and the micro:bit displays the skull image. It also sets the "unit" variable to 200 ms. This means that the LED will be on for 200 ms when emitting a _dot_, and for 600 ms when emitting a _dash_.

When the "on start" event finishes, the "forever" loop starts. It calls the "dot" function 3 times, then the "dash" function 3 times, then the "dot" function again 3 times. Last, the loop pauses for 7 times the time unit, which is equivalent to the space between words in the Morse code. Then the "forever" loop starts over and emits the SOS signal again and again, until the micro:bit is turned off.

Try experimenting with the program and emit other signals as Morse code. Can you emit your name as Morse code?