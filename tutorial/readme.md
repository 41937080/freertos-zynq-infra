# Tutorials for FreeRTOS Zynq BSP

## Introduction

A complete Zynq design includes Vivado + SDK.

- A hardware **(hw)** is generated in Vivado by adding IP blocks, one of the most important IP is the Zynq Processing System (PS). A board definition file (bdf) is (required) installed to initialize the PS and its peripherals. Then, the block design is synthezed, place and routed (PAR) and a bitstream (bit) is generated. The whole `hw` is then exported using `export hardware` file menu.
- A software **(sw)** is designed using SDK. You may write your program using barebone (standalone) or using a real time operating system (RTOS).

Therefore, the design on zynq is a combination of hw and sw, so do this tutorial!

This tutorial is based on the `Microzed` development board by Avnet. However, any board featured Zynq (include Zynq 7000 and Zynq 7000S) can all be used whereas the pin configurations must be modified accordingly.

**Note:** the official tutorial by avnet is highly recommended, See. http://zedboard.org/support/design/1519/10

## Design Flow

In each tutorial, there is a `hw` folder and a `sw` folder.

- If only PS and MIO is required , then the `hw` can be generated with only a PS IP block and design automation. No external PL logic or user defined IP blocks is required.
- If the design requires PL fabric. Then usually a carrier card (for example, the Microzed FMC, Microzed IO, or Microzed Breakout) is required to powering up the PL IO. And then, you should learn some VHDL syntax for FPGA coding. A user customized PL IP block is required in the hardware.

For simplyfy your design process, a hardware `.tcl` (tickle) script is provided in the `hw` folder. You may `source` this file in the tcl console of Vivado, and then the corresponding hardware design block is generated for you. You need then, synthesis it, PAR and generate the bit stream. Export it to SDK, and develop you project using RTOS in SDK.

## Install Vivado on linux

Hint: The following instructions are only for archlinux

  1. install `ncurses5-compat-libs` from AUR
  2. install vivado from xilinx websites, you may need to fix your local time and time zone before installing
  3. install `digilent-adept-runtime` from AUR
  4. sudo and run the script in `install_drivers` under Vivado folder
  5. plug and un-plug the usb cable
  6. Try to generate a simple program, and download it to the board

## How to contribute to this tutorial

You my fork this project and add your tutorial, test it, and pack up the hardwares in a tcl script.

Commit a pull request and ALL is done!
