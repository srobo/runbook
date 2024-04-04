# Power Board

![Power Board LEDs](https://raw.githubusercontent.com/srobo/power-v4-hw/master/test/figure1.png)

!!! note

    The boards pictured above is an early prototype and may differ from the current boards, it is only used to display the locations of the LEDs.

The fan on the power board is temperature controlled so will not spin until the board is detected to be above 40°C.

## Power Board LEDs

- DS1 - red/green
    - green is lit when the board is powered on and not in undervoltage-lockout (9.6V falling threshold, 11.1V rising threshold), this is connected to the 3.3V regulator so shows it is functional.
    - red is flashed when the battery reaches a soft undervoltage-lockout (10.2V).
- DS2 - green
    - lit when the 5V output is enabled and functional, this is connected to the 5V regulator output. 
- DS3-8 - red/green
    - green is lit when an output is enabled, this is connected to the rail so shows the actual state of the output.
    - red is lit when the port exceeds its current limit, which is latching.
- DS9 - red/green, run/error
    - green is lit initially and during USB reset. This LED can be controlled over the USB.
    - red is lit initially and during USB reset. This LED can be controlled over the USB.
