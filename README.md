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
