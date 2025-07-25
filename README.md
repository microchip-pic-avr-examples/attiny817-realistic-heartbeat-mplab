<!-- Please do not change this logo with link -->
[![MCHP](images/microchip.png)](https://www.microchip.com)

# Realistic Heartbeat

This example outputs a PWM signal to an LED, where the duty cycle of the PWM signal is dynamically increased or decreased to change the brightness of the LED in order to mimic a heartbeat. The LED pulsates 100% independently of the CPU after the initial setup with a configurable Beats Per Minute (BPM). This is done by using three of the core independent peripherals of the ATtiny817: TCB, TCD and CCL. After the initial setup, the CPU is turned off by using the idle sleep mode, while the LED continues to pulsate.

This example is programmed bare metal, i.e. no Atmel START drivers. Another version of the example with START drivers is also available.

If the example is run on the ATtiny817 Xplained Pro Development Board, the LED0 will mimic the heartbeat. If just the ATtiny817 is being used, connect the anode (+) of an LED to VCC and cathode (-) to PB4 to see the same result. The example should also work with other devices in the tinyAVR-1 Series, but might require reconfiguring the output pin. 

Included in the example is a function for changing the BPM and pulse length during run-time. The main file includes a detailed explanation of how the example works. Look at the set_heartbeat_BPM()-function in order to see how it is implemented in practice. 

## Related Documentation

- [ATtiny817 Device Page](https://www.microchip.com/wwwproducts/en/ATtiny817)

## Software Used

- [MPLAB® X IDE](http://www.microchip.com/mplab/mplab-x-ide) 6.25 or later
- [ATtiny DFP](http://packs.download.atmel.com/) 3.3.272 or later
- [MPLAB® XC8](http://www.microchip.com/mplab/compilers) 3.00 or later
- [AVR/GNU C Compiler](https://www.microchip.com/mplab/avr-support/avr-and-arm-toolchains-c-compilers) 5.4.0 or later

## Hardware Used

- [ATtiny817 Xplained Pro](https://www.microchip.com/DevelopmentTools/ProductDetails/attiny817-xpro)
- Micro-USB cable (Type-A/Micro-B)

## Operation

1. Connect the ATtiny817 Xplained Pro board to the PC using the USB cable.

2. Download the zip file or clone the example to get the source code.

3. Open the project in MPLAB X IDE.

4. Build the solution and program the ATtiny817. 

5. Observe that the LED0 pulsates like a heartbeat on the board.

## Conclusion
The example has now shown how to use core independent peripherals to create a pulsating PWM signal that increase and decrease the brightness of an LED in order to mimic a heartbeat pulse, 100% free of the CPU after the initial set-up.
