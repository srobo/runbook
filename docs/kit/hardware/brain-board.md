# Brain Board (Raspberry Pi)

![Raspberry Pi 4](https://upload.wikimedia.org/wikipedia/commons/f/f1/Raspberry_Pi_4_Model_B_-_Side.jpg)

There are two LEDs on the Raspberry Pi itself: `PWR` and `ACT`. Both are located on the lower left side of the board.

The LEDs on the KCH can also provide indication as to the state of the Raspberry Pi.

### Power LED (red)

The red `PWR` LED broadly indicates that there is 5V power to the Raspberry Pi.

Unlike other Raspberry Pi models, on a Raspberry Pi 4 the `PWR` LED is fully under the control of a GPIO expander, and when booting this IO expander is reset, causing the `PWR` LED to blink off on reboot. On booting the bootloader enables it again.

But if the PWR LED goes off (blinks) at any other time it means have an unfit power supply/power cable. 

In short, the PWR LED should be always on except for a very short time just before a reboot happens.

### Activity LED (Green)

The green `ACT` LED will flash "randomly" during normal usage and indicates access to the SD card.

If the Pi fails to boot, the `ACT` LED should flash in a pattern. If the `ACT` LED does not turn on, even though the `PWR` LED does, this indicates that the EEPROM is corrupt. It may be fixed using the `recovery.bin` method, which can be performed using [Raspberry Pi Imager](https://www.raspberrypi.com/software/).

The `ACT` LED patterns are listed in a table below, which was compiled from a variety of sources. The probable reasons have been written specifically for the runbook.

| Long Flashes | Short Flashes | Status                        | Probable reason                       |
|--------------|---------------|-------------------------------|---------------------------------------|
| 0            | 3             | Generic failure to boot       | Unknown                               |
| 0            | 4             | start*.elf not found          | Corrupted SD Card. Re-flash           |
| 0            | 7             | Kernel image not found        | Corrupted SD Card. Re-flash           |
| 0            | 8             | SDRAM failure                 | Hardware failure                      |
| 0            | 9             | Insufficient SDRAM            | Fluke. Try rebooting                  |
| 0            | 10            | In HALT state                 | Pi was shut down.                     |
| 2            | 1             | Partition not FAT             | Corrupted SD Card. Re-flash           |
| 2            | 2             | Failed to read from partition | Corrupted SD Card. Re-flash           |
| 2            | 3             | Extended partition not FAT    | Corrupted SD Card. Re-flash           |
| 2            | 4             | File signature/hash mismatch  | Corrupted SD Card. Re-flash           |
| 3            | 1             | SPI EEPROM error              | Reboot. If persists, use recovery.bin |
| 3            | 2             | SPI EEPROM is write protected | Fluke. Try rebooting                  |
| 3            | 3             | I2C error                     | Fluke. Try rebooting                  |
| 3            | 4             | Invalid secure-boot config    | Corrupted SD Card. Re-flash           |
| 4            | 4             | Unsupported board type        | Corrupted EEPROM. Use recovery.bin    |
| 4            | 5             | Fatal firmware error          | Corrupted EEPROM. Use recovery.bin    |
| 4            | 6             | Power failure type A          | Hardware failure                      |
| 4            | 7             | Power failure type B          | Hardware failure                      |
