## Outline Deluxe - a GEGL Gimp plugin specially intended for Gimp 2.99.19+ 
(but will work on 2.10)

Congratulations, this is the first GEGL plugin I made with the intent to work with CMYK Student's outline only Gimp build.

![image](https://github.com/LinuxBeaver/Outline-Deluxe-Gimp-Plugin/assets/78667207/aed42c67-9e59-4ceb-9bdb-22ddfc671f35)


## Location to put binaries (they don't go in the normal plugins folder)

### Windows

 C:\Users\(USERNAME)\AppData\Local\gegl-0.4\plug-ins
 
### Linux 

 /home/(USERNAME)/.local/share/gegl-0.4/plug-ins
 
### Linux (Flatpak includes Chromebook)

 /home/(USERNAME)/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins

## After putting binaries in the correct Location

Then restart Gimp and go to GEGL operation and look for "Outline Deluxe" if you are on Gimp 2.10

In Gimp 2.99.16+ it will be in the main menu under "filters>text styling" but also it will still exist in GEGL Operation drop down list.

## Compiling and Installing

### Linux

To compile and install you will need the GEGL header files (`libgegl-dev` on
Debian based distributions or `gegl` on Arch Linux) and meson (`meson` on
most distributions).

```bash
meson setup --buildtype=release build
ninja -C build

```
### Windows

The easiest way to compile this project on Windows is by using msys2.  Download
and install it from here: https://www.msys2.org/

Open a msys2 terminal with `C:\msys64\mingw64.exe`.  Run the following to
install required build dependencies:

```bash
pacman --noconfirm -S base-devel mingw-w64-x86_64-toolchain mingw-w64-x86_64-meson mingw-w64-x86_64-gegl
```

Then build the same way you would on Linux:

```bash
meson setup --buildtype=release build
ninja -C build
```

then put the .so or .dll binary file in the correct location listed above in "#location to put binaries"

