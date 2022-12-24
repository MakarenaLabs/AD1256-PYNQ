# AD1256 on PYNQ Z2 board
In this repo we provide a design to implement AD1256 module with PYNQ. The design was created with Vivado 2022.2.

Here we find the xsa package, which contains bitstream and hwh files in order to be used in the provided jupyter notebook.

We expose GPIO and SPI through PMODB interface.

Constraints are built as follow:
```
set_property -dict {PACKAGE_PIN W14 IOSTANDARD LVCMOS33} [get_ports spi_io1_io]
set_property -dict {PACKAGE_PIN Y14 IOSTANDARD LVCMOS33} [get_ports spi_io0_io]
set_property -dict {PACKAGE_PIN T11 IOSTANDARD LVCMOS33} [get_ports spi_sck_io]
set_property -dict {PACKAGE_PIN T10 IOSTANDARD LVCMOS33} [get_ports spi_ss_io]

set_property -dict {PACKAGE_PIN V16 IOSTANDARD LVCMOS33} [get_ports gpio0_tri_i]
set_property -dict {PACKAGE_PIN W15 IOSTANDARD LVCMOS33} [get_ports gpio1_tri_o]
```

The block design is shown in the following image

![AD1256 block design](block_design.png)
