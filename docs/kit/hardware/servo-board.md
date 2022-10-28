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
    - red is lit while the I2C interrupt routine to set the servo outputs is running. This routine hangs indefinitely if the 12V input is removed, even after it is re-enabled. In this situation the USB also locks up and since both LEDs are on gives a pink colour. This occurs after every run of the student's code since the power board outputs are disabled when their code exits. If the pink colour appears before their code has completed then there is an issue with the 12V input.
- DS11-14 - blue
    - currently unused, inaccessible over USB.
- DS15 - green
    - lit when 12V is present and the correct polarity, this is connected to the 5.5V SMPS output so shows it is functional as well. If the 12V input is wired backward this will not light.
- DS16 - green
    - lit when either an input is provided to the auxiliary header or the 5V regulator is linked to the power output for the top 4 servos. __NOTE__ The firmware is hard-coded to enable this link, __do not attach a power source to the auxiliary header__.
