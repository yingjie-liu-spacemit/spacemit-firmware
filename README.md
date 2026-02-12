# SpacemiT Firmware

This repository contains binary firmware files for SpacemiT SoCs.

## DDR Training Firmware

`ddr_fw.bin` is the DDR memory training firmware. It is loaded and
executed by U-Boot SPL during early boot to initialize DRAM.

### Usage

Pass the firmware path via the `DDR_FW_FILE` environment variable when
building U-Boot:

```sh
export DDR_FW_FILE=/path/to/spacemit-firmware/<soc>/<version>/ddr_fw.bin
make <board>_defconfig
make
```

### More information

See the U-Boot upstream patch series for each SoC:

- **K1**: https://lore.kernel.org/u-boot/20260210151459.2348758-1-raymondmaoca@gmail.com/

## Discussion

For discussions about SpacemiT U-Boot, please CC the mailing list:
u-boot-spacemit@groups.io

Archive: https://groups.io/g/u-boot-spacemit/messages
