# WIP, to be adapted from [wireguard-fpga](https://github.com/chili-chips-ba/wireguard-fpga) project

## Hardware / Software partititonig
![HW/SW partitioning](0.doc/pcie-ep-rtl-cpu-partitioning.webp)

## Hardware Architecture and Theory of Operation
![HW block diagram](0.doc/pcie-ep-rtl-architecture.webp)

The hardware architecture essentially follows the HW/SW partitioning and consists of two domains: a soft CPU for the control plane and RTL for the data plane.

The soft CPU is equipped with a Boot ROM for interfacing with off-chip memory. External memory is exclusively used for control plane processes and does not store packets. The connection between the control and data planes is established through a CSR-based HAL, which is also an interface to the Application Layer software.

The data plane consists of several cores, including Transaction Layer (TL), Data Link Layer (DL), PIPE interface

## Hardware Data Flow

### App-2-Transaction Layer (TL) interface and data flow

### TL-2-DataLink (DL) Layer (TL) interface and data flow

### DL-2-PIPE interface


### UART Data Flow
See [wireguard-fpga](https://github.com/chili-chips-ba/wireguard-fpga/tree/main/1.hw#uart-data-flow) for complete detail
