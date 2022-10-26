---
original:
  authors: Will Barber
---
# Hardware Debugging

Note: The boards pictured below are early prototypes and may differ from the current boards, the are only used to display the locations of the LEDs.

## Odroid

### Odroid LEDs

- Power - red
    - lit when the barrel jack is supplying 5V to the board.
- Alive - blue
    - flashes when the operating system is running.

## Power Board

![Power Board LEDs](https://raw.githubusercontent.com/srobo/power-v4-hw/master/test/figure1.png)

### Power Board LEDs

- DS1 - red/green
    - green is lit when the board is powered on and not in undervoltage-lockout (9.6V falling threshold, 11.1V rising threshold), this is connected to the 3.3V regulator so shows it is functional.
    - red is flashed when the battery reaches a soft undervoltage-lockout (10.2V).
- DS2 - green
    - lit when the 5V output is enabled and functional, this is connected to the 5V regulator output. The 5V is enabled whenever the board is powered on and not in any undervoltage-lockout or overcurrent situation. The 5V rail current is not currently monitored so this light going off without the whole board turning of means the regulator has been overloaded (4.2A typical).
- DS3-8 - red/green
    - green is lit when an output is enabled, this is connected to the rail so shows the actual state of the output.
    - red is lit when the port exceeds its current limit.
- DS9 - red/green, run/error
    - green is lit initially and during USB reset. This LED can be controlled over the USB.
    - red is lit initially and during USB reset. This LED can be controlled over the USB.

## Motor Board

![Motor Board LEDs](https://raw.githubusercontent.com/srobo/motor-v4-hw/master/test/led_diagram.jpg)

__Note:__ The schematic has motors 0 and 1 reversed from the silkscreen and code.

### Motor Board LEDs

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

## Servo Board

![Servo Board LEDs](https://raw.githubusercontent.com/srobo/servo-v4-hw/master/test/figure1.png)

### Servo Board LEDs

- DS1 - green
    - lit when 5V is present from either the USB or UART header, this is connected to the 3.3V regulator output so shows it is functional as well.
- DS2-9 - blue
    - currently unused, inaccessible over USB.
- DS10 - red/blue
    - blue is lit as soon as the firmware finishes initialisation.
    - red is lit while the I2C interrupt routine to set the servo outputs is running. This routine hangs indefinitely if the 12V input is removed, even after it is re-enabled. In this situation the USB also locks up and since both LEDs are on gives a pink colour. This occurs after every run of the student's code since the power board outputs are disabled when their code exits. If the pink colour appears before their code has completed then there is an issue with the 12V input.
- DS11-14 - blue
    - currently unused, inaccessible over USB.
- DS15 - green
    - lit when 12V is present and the correct polarity, this is connected to the 5.5V SMPS output so shows it is functional as well. If the 12V input is wired backward this will not light.
- DS16 - green
    - lit when either an input is provided to the auxiliary header or the 5V regulator is linked to the power output for the top 4 servos. __NOTE__ The firmware is hard-coded to enable this link, __do not attach a power source to the auxiliary header__.
