# RG405M-Linux

Linux bring-up for the Anbernic RG405M (Unisoc T618 / UMS512),
based on the existing work in beebono/rg-rotate-linux.

Long-term goal: stable RG405M Linux support followed by
integration into ROCKNIX.

## Documentation

- [Build and development environment](docs/build.md)
- [RG405M hardware notes](docs/hardware.md)

Read documentation only when it is relevant to the current task.

## Guidelines

- Make the smallest change required by the task.
- Preserve existing RG Rotate support.
- Prefer targeted searches (`rg`, `git grep`) over reading large source trees.
- Prefer microSD for early bring-up.
- Do not modify eMMC unless explicitly requested.
- Do not present unverified hardware assumptions as facts.
- Ask when an ambiguity can materially change the implementation.
