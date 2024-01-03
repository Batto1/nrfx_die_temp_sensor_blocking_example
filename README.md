# Introduction
- Example or hal libs aren't created by the given author. Only some modification in the code is made for demonstration purposes.
- original example path in Nordic NCS: modules\hal\nordic\nrfx\samples\src\nrfx_temp
- some modified information from the original example's README is given below.

# TEMP blocking example overview 

The sample demonstrates a functionality of the nrfx_temp driver operating in the blocking mode.
## Requirements

The sample supports the following development kits:

| **Board**           | **Support** |
|---------------------|:-----------:|
| nrf52dk_nrf52832    |     Yes     |
| nrf52833dk_nrf52833 |     Yes     |
| nrf52840dk_nrf52840 |     Yes     |
| nrf5340dk_nrf5340   |     Yes     |
| nrf9160dk_nrf9160   |      No     |
## Overview

Application initializes the nrfx_temp driver and starts operating in the blocking mode.
Temperature is measured until a number of measurements performed is equal to the value specified by the user.
Time to take some readings are measured and printed at the end. 

> For more information, see the die temp sensor chapter in the product specification of SoC. 

## Wiring
To run this sample, no special configuration is needed.
You should monitor the output from the board to check if it is as expected.

## Building and running
To run this sample, use nRF Connect for SDK, import your project, build and flash to your device.
