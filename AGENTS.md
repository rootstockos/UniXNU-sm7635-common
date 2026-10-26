# Agent instructions

This repository owns shared SM7635 resources and platform operations. Keep board peripherals, firmware selection,
partition layout and power policy in the device repository. Every hardware value names its source (file and line, or a
live device-tree observation).

Read these UniXNU pages before editing:

1. [Porting](https://unixnu.com/porting/)
2. [Device repositories](https://unixnu.com/porting/device-repository)
3. [SoC support](https://unixnu.com/porting/soc-support)
4. [Device trees](https://unixnu.com/porting/device-tree)
5. [Driver matching](https://unixnu.com/drivers/device-tree-matching)

Run builds from the UniXNU checkout:

```sh
./unixnu defconfig asteroids_defconfig --device ../UniXNU-asteroids
./unixnu tree --device ../UniXNU-asteroids
./unixnu build kernel --device ../UniXNU-asteroids
```

Write concise English describing current behavior.
