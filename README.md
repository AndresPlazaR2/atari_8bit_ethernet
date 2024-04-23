# Atari 8-Bit Ethernet

This repository contains the documents for an Atari 8-bit computers' cartdrige that provides an ethernet adapter.

It is based on Mark Dusko's [Atari 8-Bit Ethernet Project](https://www.atari8ethernet.com/index.html). The main difference is that
the original project used an [IP Dragon II board](https://www.atari8ethernet.com/hardware/IP_DragonII_Datasheet.pdf), now
discontinued.

This project uses the [Olimex CS8900A-H](https://github.com/AndresPlazaR2/atari_8bit_ethernet/datasheets/CS8900A-H.pdf) that can be acquired in [their website](https://www.olimex.com/Products/Modules/Ethernet/CS8900A-H/). Because this board works with 3.3V (and the Atari works with 5V), I needed to add circuitry to
do the voltage translation. That was based on Andre Fachat's [ethernet board](http://www.6502.org/users/andre/csa/etholi/index.html) for his CS/A computer.

Because not everybody feels comfortable soldering SMD components, I decided to minimize the use of them, that's why the only ones are the [SN74LVC8T245](https://github.com/AndresPlazaR2/atari_8bit_ethernet/datasheets/SN74LVC8T245.pdf); all the other components are THT (through hole).

The Olimex CS8900A-H and the IP Dragon II boards use the same chipset ([Cirrus Logic's CS8900A](https://github.com/AndresPlazaR2/atari_8bit_ethernet/datasheets/CS8900A.pdf)), and they are connected on a similar way to the cartdrige port, so the software to use one card is fully compatible with the other one. Some can be found in the [download section of the Atari 8-Bit Ethernet Project](https://www.atari8ethernet.com/Download.html).

The directories are self explanatory (I think); if there is any clarification needed let me know.

On April 2024 I finished the design and testing of the PCB for this card:
![PCB working](/pictures/working_2.jpg)
![PCB and populated board](/pictures/PCB_and_populated.jpg)

You can find more pictures of it in the `pictures` directory, and the Gerber files to build it in `gerber`.

Here is a picture of the development/prototype board:
![development and protoype board](/pictures/dev_prototype.jpg)
