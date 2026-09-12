# RG405M hardware

Hardware notes for the Anbernic RG405M.

This document should contain confirmed hardware facts useful for Linux
bring-up.

Do not record assumptions as confirmed facts.

## Platform

Device:

```text
Anbernic RG405M
```

SoC:

```text
Unisoc T618
```

Platform family:

```text
UMS512
```

Reference device used by the base project:

```text
Anbernic RG Rotate
```

Both devices use the same SoC family, but board-level wiring and
peripherals must be verified independently.

## Display

Status: not investigated yet.

Panel: unknown

DSI configuration: unknown

Backlight: unknown

## Touchscreen

Status: not investigated yet.

Controller: unknown

Interrupt GPIO: unknown

Reset GPIO: unknown

## Input

Status: not investigated yet.

Buttons: unknown

Analog sticks: unknown

Gamepad/input controller: unknown

## Storage

Status: not investigated yet.

eMMC: unknown

microSD: unknown

## Wi-Fi / Bluetooth

Status: not investigated yet.

Chip: unknown

Bus: unknown

GPIO/regulator wiring: unknown

## Audio

Status: not investigated yet.

Codec: unknown

Amplifier: unknown

Speakers/headphone routing: unknown

## Power

Status: not investigated yet.

PMIC: unknown

Battery / fuel gauge: unknown

Charger: unknown

## USB

Status: not investigated yet.

Controller configuration: unknown

USB-C role handling: unknown

## Sources

Add evidence next to hardware facts when they become known, for example:

- RG405M stock Device Tree
- stock Android kernel source
- kernel boot log
- sysfs information from the device
- physical inspection
- datasheet

Prefer primary evidence over assumptions based on RG Rotate.
