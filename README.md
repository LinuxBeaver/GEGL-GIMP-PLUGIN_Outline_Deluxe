## Outline Deluxe - a GEGL Gimp plugin specially intended for Gimp 2.99.19+ 
(but will work on 2.10)

Congratulations, this is the first GEGL plugin I made with the intent to work with CMYK Student's outline only Gimp build.

![image](https://github.com/LinuxBeaver/Outline-Deluxe-Gimp-Plugin/assets/78667207/bd7c761c-9847-44b0-a2ae-6609b15bbf37)


![image](https://github.com/LinuxBeaver/Outline-Deluxe-Gimp-Plugin/assets/78667207/aed42c67-9e59-4ceb-9bdb-22ddfc671f35)

## Co-Dependencies of Outline Deluxe 
This plugin ships with two other plugins of mine needed for it to work. Said plugins are 'SSG' and 'Custom Bevel'. Said plugins are both included in the source code and binaries. So there is no mistake that the user won't get them.

![image](https://github.com/LinuxBeaver/Outline-Deluxe-Gimp-Plugin/assets/78667207/f0caea93-cb9c-46f7-a45a-45289f097c7d)
![image](https://github.com/LinuxBeaver/Outline-Deluxe-Gimp-Plugin/assets/78667207/d6bb82a6-9fae-4cf9-a158-247d8c9a5e9a)



## Location to put binaries (they don't go in the normal plugins folder)

### Windows

 C:\Users\(USERNAME)\AppData\Local\gegl-0.4\plug-ins
 
### Linux 

`~/.local/share/gegl-0.4/plug-ins`
 
### Linux (Flatpak includes Chromebook)

`~/.var/app/org.gimp.GIMP/data/gegl-0.4/plug-ins`

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

