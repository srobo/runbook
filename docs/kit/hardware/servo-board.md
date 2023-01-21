# Servo Board

![Servo Board LEDs](https://raw.githubusercontent.com/srobo/servo-v4-hw/master/test/figure1.png)

!!! note

    The boards pictured above is an early prototype and may differ from the current boards, it is only used to display the locations of the LEDs.

## Servo Board LEDs

- DS1 - green
    - lit when 5V is present from either the USB or UART header, this is connected to the 3.3V regulator output so shows it is functional as well.
- DS2-9 - blue
    - currently unused, inaccessible over USB.
- DS10 - red/blue
    - blue is lit as soon as the firmware finishes initialisation.
    - red is lit while the I2C interrupt routine to set the servo outputs is running.
- DS11-14 - blue
    - currently unused, inaccessible over USB.
- DS15 - green
    - lit when 12V is present and the correct polarity, this is connected to the 5.5V SMPS output so shows it is functional as well. If the 12V input is wired backward this will not light.
- DS16 - green
    - lit when either an input is provided to the auxiliary header or the 5V regulator is linked to the power output for the top 4 servos. __NOTE__ The firmware is hard-coded to enable this link, __do not attach a power source to the auxiliary header__.

## Pink LED of Death "PLOD" Bug

When the 12V input is removed, the I2C interrupt routine will hang indefinitely, even after the input is restored.

In this situation, both the red and blue components of DS10 will turn on, which appears as a pink colour (despite actually being separate red and blue). The USB will also lock up, manifesting as `Pipe Error` in Python stack traces if the code tries to access the board.

This situation will occur after every run of code on the robot as the 12V outputs on the power board are disabled when code exits. If the pink colour appears before their code has completed then there is an issue with the 12V input.

There is a workaround in the kit software that attempts to mitigate the impacts of this bug, called [Servohack](../../software/#servohack).