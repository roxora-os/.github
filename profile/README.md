# Roxora

Roxora builds images for Rockchip boards that pair Armbian's kernel and bootloader with a stock Ubuntu userspace.

Armbian does the hard part: kernels, U-Boot and board support for a long list of Rockchip boards. Its images also put Armbian's own userland on top, with its first-run wizard, config tool and defaults. Some people just want plain Ubuntu on the board. Roxora keeps Armbian's hardware packages and replaces the rest with what you would get from Ubuntu itself, so userspace updates come straight from the Ubuntu archive.

## Status

Early. Pre-release images for the Radxa ROCK 4D and the ArmSoM CM5-IO on Ubuntu 24.04 are built and checked in CI; they have not been booted on hardware yet. Downloads and the list of boards are on the website: https://roxora-os.github.io

## How it works

The build is an Armbian extension, not a fork. Kernel, device tree, U-Boot and firmware packages still come from Armbian, and apt is pinned so only those packages are taken from Armbian's repository. Everything else comes from Ubuntu.

## Contact

Issues and pull requests go to the build repository: https://github.com/roxora-os/build

Email: oss@gahingwoo.com

Roxora is based on Ubuntu and Armbian. It is not affiliated with or endorsed by Canonical, the Armbian project or Rockchip.
