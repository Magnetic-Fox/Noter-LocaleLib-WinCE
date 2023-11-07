# Locale Library Definition for Noter Client (Windows CE)

This repository contains very simple codes for creating DLL with string table for chosen language.

## What is included in this repo?

Simple Pascal code which main goal is to include resource script code only.
The main part is, of course, the resource, which contains a string table defining the locale.
Here it is in Polish version.

## What is needed to compile these codes?

Lazarus IDE with additional FPC cross-compilation distributions (for `ARM/WinCE` or even `x86-64`).
The code compiles without any errors under Lazarus 1.2.6 with FPC 2.6.4 both for Mobile and Desktop versions of Windows (both being 32- and 64-bit distributions).
Haven't tested under newer Lazarus versions (as the code was developed under Windows 2000).

It is possible to port this solution to eMbedded Visual C++ (or other compiler suite), as the main code is only a Pascal stub.
The only thing needed is a plain empty DLL file which can be linked with resource containing string table - this can probably be achieved by any good compiler that support Windows target.

**Remember, that Noter Client for Windows CE uses UTF-8. If You wish to port this library to other language for use with, let's say - older, compiler, You'll have to encode strings in resource to UTF-8 form before.**

## Known problems

You can use Ultimate Packer for eXecutables, but only for desktop Windows distributions.
Packed DLL refuses to work properly under Windows Mobile 6.5 (Noter has no labels after loading).
For Windows CE/Mobile targets, make sure not to use UPX. 

## Tests information

Depending on the platform for which the program was compiled, it was tested on:

* Windows Mobile 6.5 (ARM version)
* Windows 2000/XP (x86 version)
* Linux Mint/macOS Monterey (Wine - x64 version)

None of the version above caused any problems on the mentioned OS-es.

## Disclaimer

I've made much effort to provide here working and checked codes with hope it will be useful.
**However, these codes are provided here "AS IS", with absolutely no warranty! I take no responsibility for using them - DO IT ON YOUR OWN RISK!**

## License

Codes provided here are free for personal use.
If you like to use any part of these codes in your software, just please give me some simple credits and it will be okay. ;)
In case you would like to make paid software and use parts of these codes - please, contact me before.

*Bartłomiej "Magnetic-Fox" Węgrzyn,
November 7, 2023*
