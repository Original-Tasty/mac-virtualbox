

# HOW TO INSTALL

## First, install Ubuntu and VM Virtual Box:

### Install Ubuntu on Windows 10:

![Ubuntu for Windows 10](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab)


### Install  VM Virtual Box on Windows 10:

![VM Virtual Box 6.1.16 for Windows 10](https://download.virtualbox.org/virtualbox/6.1.16/VirtualBox-6.1.16-140961-Win.exe)

--------------

## Start Ubuntu in Windows 10

### Once there type in the command below:

      curl https://raw.githubusercontent.com/Original-Tasty/mac-virtualbox/master/macos-guest-virtualbox.sh | bash

#### Follow the instructions from the script. 

#### To edit the Mac os specifications, edit the file "macos-guest-virtualbox.sh"


#### macOS Catalina (10.15), Mojave (10.14), and High Sierra (10.13) currently supported.

--------------

# Dependencies

The following dependencies should be available through a package manager:  
`bash` `coreutils` `gzip` `unzip` `wget` `xxd` `dmg2img`  `virtualbox`

The following optional packages provide optical character recognition that reduces the required interaction with the script:  
`tesseract-ocr` `tesseract-ocr-eng`

--------------

Supported versions:

* [VirtualBox](https://www.virtualbox.org/wiki/Downloads) ≥ 6.1.6, though versions as low as 5.2 may work.
* GNU `Bash` ≥ 4.3, on Windows run through [Cygwin](https://cygwin.com/install.html) or WSL - see [NEM](#virtualbox-native-execution-manager-nem)
* GNU `coreutils` ≥ 8.22, GNU `gzip` ≥ 1.5, Info-ZIP `unzip` ≥ v6.0, GNU `wget` ≥ 1.14, `xxd` ≥ 1.11
* `dmg2img` ≥ 1.6.5, on Cygwin the package is not available through the package manager so the script downloads it automatically.
* `tesseract-ocr` ≥ 4

--------------

# Documentation

Documentation can be viewed by executing the command `./macos-guest-virtualbox.sh documentation`

The majority of the script is either documentation, comments, or actionable error messages, which should make the script straightforward to inspect and understand.

--------------

# Primary display resolution

The following primary display resolutions are supported by macOS on VirtualBox: `5120x2880` `2880x1800` `2560x1600` `2560x1440` `1920x1200` `1600x1200` `1680x1050` `1440x900` `1280x800` `1024x768` `640x480`. See the [documentation command](#documentation) for further information.

--------------

# Unsupported features

Developing and maintaining VirtualBox or macOS features is beyond the scope of this script. Some features may behave unexpectedly, such as USB device support, audio support, FileVault boot password prompt support, and other features.

--------------

# Performance and deployment

After successfully creating a working macOS virtual machine, consider importing it into more performant virtualization software, or packaging it for configuration management platforms for automated deployment. These virtualization and deployment applications require additional configuration that is beyond the scope of the script.

QEMU with KVM is capable of providing virtual machine hardware passthrough for near-native performance. QEMU supports the `VMDK` virtual disk image storage format, which can be configured to be created by the script. See the [documentation command](#documentation) for further information. QEMU and KVM require additional configuration that is beyond the scope of the script.

--------------

