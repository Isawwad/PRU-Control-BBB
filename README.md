# PRU-Control-BBB
Documentation for PRU processor control in beagle boards - am335x specific
# PRU CONTROL FOR cortex am335x

First, we will look into the general process of using the PRU to control a peripheral. Then, we will illustrate that process by walking through the template project PRU_ADC_onChip, 
which was written for the Sitara AM335x processor running on a BeagleBone Black board. Let's start by discussing the general process of controlling a peripheral with the PRU. In many cases,
you only want one core interacting with the peripheral. If that is the case, make sure that you disable your other cores from accessing the peripheral.

For example, in Linux, you can disable the ARM from accessing tThe ADC by setting the ADC as disabled in the device tree file. Next, you need to load firmware into the PRU's 
instruction RAM, or IRAM. Texas Instrument's Linux and RTOS operating systems both have tools that allow the ARM to initialize the PRU. Then, the PRU must initialize the peripheral, 
since the other cores think that the peripheral is not being used. 


## Installation
First, you will need to create an os image to your beagle bone blue board, using a host windows machine, so download pru folder , unzip it then go to "rt-linux-evm"
unzip the os image so you can load it to your beagle.

Second, download balenaEtcher application that loads os image to beagle boards : link [https://www.balena.io/etcher/].

Third, load your unzipped image to the board.


Now you need to get the ready made code from pru software support package and some how build it and load it to pru processor.

The rest of detailed instructions inside the folder "pru-sw-support-package"

## Usage
#### control peripherals independently fro Arm processor.
