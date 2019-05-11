---
layout: project
title: Adjust LED brightness
description: Shows how to change the brightness of the connected LED by writing an analog signal to the micro:bit pin. Pressing button A decreases the brightness. Pressing button B increases the brightness.
category: project
slug: adjust-led-brightness
diagram: led
makecode: _T3m6EC7dMWcw
requires: B1,S1,D1,1,3x3
---

When you close the slide switch (S1), the Battery Holder (B1) powers the snap:bit through the 3V snap and the micro:bit turns on. The “on start” event triggers and the micro:bit sets the brightness level to 5 and calls the "set brightness" function.

The "set brightness" function writes an analog signal to pin P1 to turn the LED on. The value of the analog signal determines how much current will flow from pin P1 to the LED. The more current flows, the higher the brightness of the LED is. The analog signal can take values between 0 and 1023. If analog signal 0 is written, the LED turns off. If analog signal 1023 is written, the LED lights in its full brightness. If a value like 128 is written then the LED lights in around half of its brightness.

Compare this to the digital signal used in the [Turn LED on and off using the press switch](press-switch-turns-led.html) project. Digital signal 0 is equivalent to analog signal 0, and digital signal 1 is equivalent to analog signal 1023.

The brightness of the LED does not depend on the current linearly, but rather exponentially. In other words, changing the analog value in the range between 0 and 200 is significantly more noticeable than in the range between 200 and 1023. Therefore, we use the brightness level as the exponent in this [power of 2](https://en.wikipedia.org/wiki/Power_of_two) formula: 2<sup>n</sup> - 1.

Level 0 gives 2<sup>0</sup> - 1 = 1 - 1 = 0, i.e. the LED is off.

Level 10 gives 2<sup>10</sup> - 1 = 1024 - 1 = 1023, i.e. the LED is at its full brightness.

This table shows how the brightness level is converted to the value of the analog signal sent to pin P1:

| Level | Formula                       | Value |
| ----: | :---------------------------: |-----: |
|     0 | 2<sup>0</sup>  - 1 =    1 - 1 |     0 |
|     1 | 2<sup>1</sup>  - 1 =    2 - 1 |     1 |
|     2 | 2<sup>2</sup>  - 1 =    4 - 1 |     3 |
|     3 | 2<sup>3</sup>  - 1 =    8 - 1 |     7 |
|     4 | 2<sup>4</sup>  - 1 =   16 - 1 |    15 |
|     5 | 2<sup>5</sup>  - 1 =   32 - 1 |    31 |
|     6 | 2<sup>6</sup>  - 1 =   64 - 1 |    63 |
|     7 | 2<sup>7</sup>  - 1 =  128 - 1 |   127 |
|     8 | 2<sup>8</sup>  - 1 =  256 - 1 |   255 |
|     9 | 2<sup>9</sup>  - 1 =  512 - 1 |   511 |
|    10 | 2<sup>10</sup> - 1 = 1024 - 1 |  1023 |

<br>
The "set brightness" function uses the 2<sup>n</sup> - 1 formula to convert the current brightness level (the "level" variable) to the analog value to be written to pin P1. The "set brightness" function also plots the current brightness level to the LED screen of the micro:bit as an extra visual indication.

Pressing button A on the micro:bit decreases the current brightness level by 1 and calls the "set brightness" function to update the brightness of the LED. Note the "if" statement that limits the minimum brightness level to 0.

Pressing button B on the micro:bit increases the current brightness level by 1 and calls the "set brightness" function to update the brightness of the LED. Note the "if" statement that limits the maximum brightness level to 10.