## Development host

Host OS: Windows.
Linux build environment: WSL2 Ubuntu.

Kernel, U-Boot, rootfs and disk-image builds are performed inside WSL.

The repository is kept in the WSL filesystem, for example:

    ~/projects/rg405m-linux

Windows is used for host-side device interaction such as ADB and
writing completed disk images to microSD unless documented otherwise.

### Git over WSL

If GitHub smart-HTTP operations hang under WSL, force HTTP/1.1:

    git config --global http.version HTTP/1.1
