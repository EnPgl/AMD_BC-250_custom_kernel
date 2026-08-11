# Arch Linux Kernel Custom for AMD BC-250

A customized version of the Arch Linux kernel for the [AMD BC-250](https://elektricm.github.io/amd-bc250-docs/#what-is-the-bc250), with some patch and stripped of unused modules.

## Table of Contents
- [Kernel Modules](#kernel-modules)
- [Patches](#patches)
- [Build and Install](build-and-install)

## Kernel Modules
- The list of modules included in the kernel compilation is based on that of [linux-tkg](https://github.com/Frogging-Family/linux-tkg), with modifications made based on the results of [modprobed-db](https://github.com/graysky2/modprobed-db) and personal usage experience.

## Patches
- **40 CU Unlock**: from [duggasco/bc250-40cu-unlock](https://github.com/duggasco/bc250-40cu-unlock)

## Build and Install
For more information about buildind the kernel using the [Arch build system](https://wiki.archlinux.org/title/Arch_build_system, check the relative page on the [wiki](https://wiki.archlinux.org/title/Kernel/Arch_build_system).

### Building yourself
- clone the repository and cd into it
- run `updpkgsums` and the `makepkg -s MAKEFLAGS="--jobs=$(nproc)" -f`


### Installing
- after the build (or if you have decide to download the files from the releases), simply install them by running `# pacman -U linux-lts_bc-250-headers-version_number-x86_64.pkg.tar.zst linux-lts_bc-250-version_number-x86_64.pkg.tar.zst`
