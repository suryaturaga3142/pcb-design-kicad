# pcb-design-kicad
Designing PCBs is an integral skill that takes you beyond breadboarding and using dev boards. It lets you combine different components with very little latency, and makes products look awesome!

Here's a collection of some of my favorite PCBs that I really enjoyed designing on my own. I don't just go and draw stuff up. I think of a use case first, like connecting devices to my laptop or using AUX cables for STM32. Then I go about employing the skills available to me.

## flash_adc1

My own design of a flash ADC that makes use of less digital combinationl logic and more buffering and chaining of comparators to directly obtain the converted reading. It's a unique design that saves on resources by leveraging a binary search style of output.

Typical ADCs are either SAR (Successive Approximation Register), Sigma-Delta, or Flash. SAR is resource efficient and used a lot to conserve area. Flash is extremely fast but resource heavy.

Performance wise, flash interests me a fair amount. It produces a thermometer code that is then converted to digital logic, but what if there was a better way? That long line of resistors always stood out to me. This is my design of a flash ADC based on binary search, where a cascade of logic allows you to directly collect the value.

## dsp1-stm32

A single PCB with an STM32H757 controller, specialized for signal processing. It has AUX plugs, buttons, switches, and potentiometers. There are also headers and sockets for timers, ADCs, SWD, UART, and I2C.

The PCB makes use of ADCs with internal OPAMPS, the DACs for the AUX output, jumpers for easy reconfiguration, and USB-C. It also allows the use of a dedicated 5V power supply as opposed to USB-C connection.

Designing this is proving to be quite challenging! Going about designing the circuit has taught me how to build protection circuits, read datasheets, calculate component values, determining appropriate footprints and routing patterns, and much more.

This isn't one of those projects that just "ends". This is one that I'm using to push the boundaries of my skills in PCB design. As I make progress in design, new ideas form, almost as if the PCB is creating itself! 

When I started, I added communication protocol pins, and then added on ADCs and DACs with AUX plugs. Then, I learnt how to manage power in PCBs and implemented better designs to route power and make use of noise filtering.

I then began working on the finer details like estimating capacitance values for circuits (like the HSE circuit) and implementing switching voltage regulators for lower voltage power supplies.

Then, I learnt of the importance of ESD protection for signals and the various types of protection for power lines and grounds.

Going about adding on more functionality like reverse polarity protection while ensuring all the design constraints are met is quite the challenge!

## usb-demux1

This was one of the first PCBs I've designed. I have only one USB-C receptacle on my laptop, so it's hard for me to connect multiple devices like microcontrollers and FPGAs without reconnecting each and every time.

This fixes my problem, lets me switch between different devices. Even better, it's got a USB-C plug so no more USB-C to A conversion!

## bluepill1-stm32

A small project just to get the hang of some routing and setting parameters based on a PCB printing agency.