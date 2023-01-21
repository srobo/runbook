# Motor Board

![Motor Board LEDs](https://raw.githubusercontent.com/srobo/motor-v4-hw/master/test/led_diagram.jpg)

!!! note

    The schematic has motors 0 and 1 reversed from the silkscreen and code.

!!! note

    The boards pictured above is an early prototype and may differ from the current boards, it is only used to display the locations of the LEDs.

## Motor Board LEDs

- A (DS1/DS6 - green/red)
    - green is lit when USB or UART power is present
    - red is lit when there is USB activity to the USB-UART IC.
- B (DS7 - red/green)
    - green is lit when there is 12V present in the correct polarity on 12V input
    - red is lit when the 12V input has incorrect polarity
- C (DS2 - red)
    - toggled by the ADC interrupt, this should be fast enough that the LED is not visibly while the firmware is running normally.
- D (DS3 - blue)
    - currently unused, inaccessible over USB.
- E (DS4 - red)
    - currently unused, inaccessible over USB.
- F (DS5 - blue)
    - currently unused, inaccessible over USB.
- G/H (DS9 - red/blue)
    - blue is lit when motor 1 is set to move forward
    - red is lit when motor 1 is set to move backward
- I/J (DS8 - red/blue)
    - blue is lit when motor 2 is set to move forward
    - red is lit when motor 2 is set to move backward
