# Neotron Pico

The Neotron Pico is micro-ATX sized Neotron, powered by a Raspberry Pi Pico microcontroller board. The Raspberry Pi Pico is fitted with a Raspberry Pi RP2040 microcontroller - a dual-core Cortex-M0+ with 256 KiB of SRAM. The Raspberry Pi Pico also has a 2 MiB external QSPI flash.

Whilst the Cortex-M0+ cores are only ARMv6-M compatible (not ARMv7E-M or even ARMv7-M), there were some very compelling advantages in making the switch. For example, compared to the Texas Instruments Tiva-C Launchpad on the Neotron 32, the Raspberry Pi Pico:

* Has two cores instead of one
* Is clocked at 133 MHz instead of 80 MHz (and actually, many units run happily at 250 MHz)
* Has 256 KiB of SRAM instead of 32 KiB
* Costs £3.60 instead of £15.00
* Has hardware designed to generate digital RGB video
* Can drive an I²S audio codec

## Form Factor

The Neotron Pico is a micro-ATX sized board - 244mm x 170mm. It is designed to fit into any micro-ATX or ATX compatible PC case, and includes headers for a reset switch, power switch, power LED and status LED. It provides four card-edge expansion slots, which provide access to the SPI and I²C buses. Each slot has a unique IRQ line and SPI Chip Select, avoiding the classic IBM PC problem of allocating resources to expansion cards.

## Links

* Hardware: <https://github.com/Neotron-Compute/Neotron-Pico>
* BIOS: <https://github.com/Neotron-Compute/Neotron-Pico-BIOS>
* Raspberry Pi Pico
  * Datasheet: <https://datasheets.raspberrypi.org/pico/pico-datasheet.pdf>
* Raspberry Pi Silicon RP2040
  * Datasheet: <https://datasheets.raspberrypi.org/rp2040/rp2040-datasheet.pdf>
  * Hardware Design Guide: <https://datasheets.raspberrypi.org/rp2040/hardware-design-with-rp2040.pdf>

## Features

* Dual 133 MHz 32-bit ARM Cortex-M0+ CPU cores
* 256 KiB of internal SRAM
* Super-VGA output
    * 640x400, 640x480 and 800x600
    * 256 colours from a pallette of 4,096
    * RGB video buffer for genuine 75 Ohm output
    * Has ESD protection circuit with VGA DDC level-shifter
* 16-bit 48 kHz audio input and output (line-in, mic-in, line-out and headphone-out)
  * Uses Texas Instruments TLV320AIC23BPW audio code
  * Has triple 3.5mm jack, plus AC'97 header and extra four-pin line-in header
* One USB Full-speed OTG port
* Dedicated board management controller, supporting
  * Two PS/2 ports (keyboard and mouse)
  * Standby mode and PSU control
  * System reset
* SD/MMC Slot
* Four Expansion Slots (with SPI and I²C)
* MCP7940N Real-Time Clock with backup battery

## Supported video modes:

The following [video modes](./hardware_soc_video.md) are supported:

* Mode 0x00 - 80x30 text mode at 640x480
* Mode 0x01 - 80x60 text mode at 640x480
* Mode 0x10 - 80x25 text mode at 640x400
* Mode 0x11 - 80x50 text mode at 640x400
* Mode 0x91 - 80x25 text mode at 640x200
* Mode 0x05 - 640x480 in 16 colours
* Mode 0x06 - 640x480 in 4 colours
* Mode 0x07 - 640x480 in 2 colours
* Mode 0x15 - 640x400 in 16 colours
* Mode 0x16 - 640x400 in 4 colours
* Mode 0x17 - 640x400 in 2 colours
* Mode 0x94 - 640x200 in 256 colours
* Mode 0x95 - 640x200 in 16 colours
* Mode 0x96 - 640x200 in 4 colours
* Mode 0x97 - 640x200 in 2 colours
* Mode 0x8C - 320x240 in 256 colours
* Mode 0x8D - 320x240 in 16 colours
* Mode 0x8E - 320x240 in 4 colours
* Mode 0x8F - 320x240 in 2 colours
* Mode 0x9C - 320x200 in 256 colours
* Mode 0x9D - 320x200 in 16 colours
* Mode 0x9E - 320x200 in 4 colours
* Mode 0x9F - 320x200 in 2 colours
