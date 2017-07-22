# .tcl script file generating zynq hardware

  - [ ] `zynq_base.tcl` generate base example for Zynq, includes AXI Timer, Ethernet, GPIO, etc.
  - [x] `zynq_basic.tcl` generate the hw for the tutorial.
  - [ ] `zynq_dma.tcl` generate simple DMA example for Zynq, (which can also enable the scatter-gather DMA).

## Requires

1. Microzed development board, 7Z010 or 7Z020, etc.
2. The board definition files, available from zedboard.org should also be installed.

## How to use it

1. create a project folder.
2. copy the `.tcl` script to that folder.
3. open vivado, open the tcl console, and source `.tcl`

For example

```tcl
cd {D:\xeit-ng\xeit-hw\zynq_proj}
source zynq_basic.tcl
```

Then save your project.

## Note

Every line in the `tcl` script represent an operation in Vivado.
