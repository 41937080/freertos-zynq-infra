# FreeRTOS Infrastructure for Zynq (Microzed, Zedboard, etc.)

**Note: This project no longer provides the FreeRTOS bsp for Zynq. Please use the official bsp from Xilinx whenever possible.**

See:

https://github.com/Xilinx/embeddedsw

The layout of Xilinx **embeddedsw** is

```
 -- ThirdParty
  |-- bsp/freertos901_xilinx
  |-- sw_services
    |-- libmetal
    |-- lwip141
    |-- openamp
```

This infrastructure, provides additional `sw_services` such as `freertos_cli`, etc. and some demos in `sw_apps`. This project also gives hardware designs in `hw_apps` using `.tcl` script. You may generate a basic PL design in one click. There are also some tutorials (or notes) on how to use FreeRTOS under Xilinx Zynq (tested using microzed 7z010 and 7z020).

```
 -- hw_apps
  |-- zynq_basic.tcl
  |-- zynq_advanced.tcl
 -- sw_apps
  |-- 1. hello, world
  |-- 2. gpio
  |-- 3. ethernet RX/TX, iperf
  |-- 4. PL/PS programming
 -- sw_services
  |-- freertos_cli
 -- tutorials
```

## 1. Instructions

1. Create the base design in Vivado using a tcl script in `hw_apps`, synthesis and generate the bitstream.
2. Open SDK, and set repository via `Xilinx Tools`, `Repositories` and add (new) the location of the cloned source code.
3. Open `File`, `New Project`, add the demos, Select `freertos901_xilinx` as the bsp and select any related demo projects.
4. Compile and run.

