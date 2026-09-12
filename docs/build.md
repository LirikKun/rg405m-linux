# Build

This document describes the development/build environment for RG405M-Linux.

The current project is based on:

https://github.com/beebono/rg-rotate-linux

## Clone

The repository uses Git submodules.

```sh
git clone --recurse-submodules <repo-url>
```

For an existing clone:

```sh
git submodule update --init --recursive
```

## Kernel

Kernel source:

```text
src/linux-7-1-sprd/
```

Architecture:

```text
arm64
```

Cross compiler prefix:

```text
aarch64-linux-gnu-
```

The upstream project currently uses GCC 13.

Build kernel and Device Trees from the repository root:

```sh
make -C src/linux-7-1-sprd \
    ARCH=arm64 \
    CROSS_COMPILE=aarch64-linux-gnu- \
    -j"$(nproc)" \
    Image dtbs
```

Kernel output:

```text
src/linux-7-1-sprd/arch/arm64/boot/Image
```

Device Trees:

```text
src/linux-7-1-sprd/arch/arm64/boot/dts/sprd/
```

## Development boot

During early bring-up, prefer microSD boot instead of modifying eMMC.

The upstream project provides:

```sh
tools/scripts/build_sdcard_debian.sh
```

The RG Rotate development flow uses microSD for fast iteration.

Do not assume this flow works unchanged on RG405M until it has been
tested on the device.

## Generated files

Upstream uses:

```text
build/
```

for generated images and temporary build output.

Do not commit generated build artifacts unless there is a specific
reason to do so.

## RG405M status

A successful build does not mean the resulting kernel or DTB has been
validated on RG405M.

Hardware validation must be distinguished from build success.
