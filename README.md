# pcb-design-kicad
Designing PCBs is an integral skill that takes you beyond breadboarding and using dev boards. It lets you combine different components with very little latency, and makes products look awesome!

Here's a collection of some of my favorite PCBs that I really enjoyed designing on my own. I don't just go and draw stuff up. I think of a use case first, like connecting devices to my laptop or using AUX cables for STM32. Then I go about employing the skills available to me.

## usb-demux1
This is one of the first PCBs I've designed. I have only one USB-C receptacle on my laptop, so it's hard for me to connect multiple devices like microcontrollers and FPGAs without reconnecting each and every time.

This fixes my problem, lets me switch between different devices. Even better, it's got a USB-C plug so no more USB-C to A conversion!

## dsp1-stm32
My biggest project so far. A single STM32 PCB with an STM32H757 controller, specialized for signal processing. It has AUX plugs, buttons, switches, and potentiometers. There are also headers and sockets for timers, ADCs, SWD, UART, and I2C master & slave.

The PCB makes use of ADCs with internal OPAMPS, the DACs for the AUX output, jumpers for easy reconfiguration, and USB-C.

This is still going on, and designing this is proving to be quite challenging! Going about designing the circuit has taught me how to build protection circuits, read datasheets, calculate component values, determining appropriate footprints and routing patterns, and much more.

## bluepill1-stm32
A small project just to get the hang of some routing and setting parameters based on a PCB printing agency.