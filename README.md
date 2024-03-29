![Screenshot](https://i.imgur.com/6XsnJPp.png)

# rEFInd-wildside
rEFInd-wildside is a shiny black background with bold red 3d icon theme for the rEFInd UEFI Boot Manager.

[rEFInd](http://www.rodsbooks.com/refind/) is a boot manager for UEFI systems and scans for kernels & EFI at boot.

### Usage

 1. Locate your refind EFI directory. This is commonly `/boot/EFI/refind`
    though it will depend on where you mount your ESP and where rEFInd is
    installed.

 2. Create a folder called `themes` inside it, if it doesn't already exist

 3. Clone this repository into the `themes` directory as `themes/rEFInd-wildside`.

 4. To enable the theme add `include themes/rEFInd-wildside/theme.conf` at the end of
    `refind.conf`.
    
Entries should be autodetected and shown with the proper icons.

Manual entry can be done via `menuentry` option.

Example:

```
menuentry "Windows" {
	icon /EFI/refind/themes/rEFInd-wildside/icons/os_windows.png
	loader /EFI/Microsoft/Boot/bootmgfw.efi
}
```

Other examples are in the `refind.conf` file.

-------------------------------
rEFInd-wildside notes
-------------------------------

September 14, 2018: Initial release of rEFInd-wildside to DeviantArt.

December 31, 2018: rEFInd-wildside theme uploaded to github.

January 6, 2019: Added icons for Sparky Linux, GameDrift, and Lakka

March 30. 2019: Added icons for Pop OS and Pisi Linux

April 10, 2019: Added icons for Parrot Sec OS, PureOS, and Qubes OS

December 18, 2020: Added new function icons func_bootorder.png and func_install.png

March 3, 2021: Added icon for Garuda Linux

February 13,2024: Added haiku_loader.efi to enable launching the Haiku Operating System
The simplest way I have found to launch a Haiku desktop on a UEFI machine is to setup rEFInd on a USB drive as Partition 1, so it launches first, set the UEFI to launch UEFI USB devices first, and make sure I have a folder called Haiku under EFI with the file haiku_loader.efi I just updated. That will find any Haiku builds you have on your system, or at least it should. It doesn't always work, for one reason or another. But it's pretty darn good, and it's nice to have Haiku on the rEFInd menu at last! I launch from a USB drive because it holds several key applications that I may require in the event of an emergency, such as a complete system failure.

February 14,2024: Added image of common folder setup for rEFInd using haiku_loader.efi in folder Haiku under primary folder EFI.

*** Please note: These additions only work with the 64 bit version of the Haiku installer.

*** Also note: You should update to the latest version of the 64 bit Haiku installer before you attempt installation.

*** Please note: Installation will NOT work with the 32 bit installer of Haiku on a UEFI device.

