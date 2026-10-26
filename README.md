# UniXNU SM7635 support

Shared Qualcomm SM7635 (volcano, Snapdragon 7s Gen 3) support for UniXNU: CPU topology, GICv3, UFS resources, the
Adreno 810 register blocks, and XNU patches. Device repositories supply memory layout, peripherals, firmware, power policy
and packaging.

The SoC shares SM8550's GIC layout, timer, CPU numbering, PSCI method and UFS host and PHY windows. Its cores are four
Cortex-A520 and four Cortex-A720. The GPU is an Adreno 810 (gen8); its driver is board-owned for now (the asteroids device
repository's NativeAdreno), so the GPU nodes stay disabled here.

Hardware descriptions use `qcom/volcano.dtsi` at revision `e0eb1dc2235850f9f966bfb3294967d06c00a0f1` of
[android_kernel_nothing_sm7635-devicetrees](https://github.com/NullDebris/android_kernel_nothing_sm7635-devicetrees),
checked against a Nothing Phone (3a)'s live device tree.

Build through the [UniXNU CLI](https://unixnu.com/building). Read the
[device repository specification](https://unixnu.com/porting/device-repository),
[device-tree specification](https://unixnu.com/porting/device-tree) and
[component catalog](https://unixnu.com/reference/components).

## Contents

| Path | Contents |
| --- | --- |
| `soc.toml` | SoC profile and component selection |
| `configs/` | Kernel configuration fragments |
| `dts/sm7635.dtsi` | Shared hardware resources |
| `patches/xnu/series` | Ordered SoC patches (secondary CPU start, the platform power provider) |

## Devices

- Nothing Phone (3a), `asteroids`: [rootstockos/UniXNU-asteroids](https://github.com/rootstockos/UniXNU-asteroids)
