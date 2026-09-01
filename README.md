# Awesome N64 Development with stars

A curated list of Nintendo 64 development resources including toolchains, documentation, emulators, example code, and more!

## Contents

* [Community](#community)
* [Documentation](#documentation)
* [Videos](#videos)
* [Toolchains](#toolchains)
* [Assemblers](#assemblers)
* [Emulators](#emulators)
  * [Actively Maintained](#actively-maintained)
  * [Works In Progress](#works-in-progress)
  * [Unmaintained](#unmaintained)
* [Development Hardware](#development-hardware)
* [Tools and Libraries](#tools-and-libraries)
  * [Development Cartridge Loaders](#development-cartridge-loaders)
  * [Flashcart Menu Software](#flashcart-menu-software)
  * [Asset Conversion and Viewing](#asset-conversion-and-viewing)
    * [3D](#3d)
    * [2D](#2d)
  * [Audio Playback and Editing](#audio-playback-and-editing)
  * [Debugging](#debugging)
  * [ROM Manipulation](#rom-manipulation)
  * [Development Libraries](#development-libraries)
* [Reverse Engineering](#reverse-engineering)
  * [Projects](#projects)
  * [Guides and Reference](#guides-and-reference)
  * [Tools and Disassemblers](#tools-and-disassemblers)
* [Programming](#programming)
  * [Assembly](#assembly)
  * [C](#c)
    * [Guides](#guides)
    * [Example Code](#example-code)
  * [Rust](#rust)
  * [Go](#go)

## Community

* [N64brew](https://discord.gg/WqFgNWf) - Nintendo 64 homebrew chat on Discord
* [Discord64](https://discord.gg/sSkQTBpFhv) - Nintendo 64 emulation and homebrew chat on Discord
* [`#n64dev` on EFnet](http://chat.efnet.org/?channels=n64dev) - Nintendo 64 development IRC channel on EFnet
* [/r/N64Homebrew](https://www.reddit.com/r/N64Homebrew/) - The N64Homebrew subreddit
* [Nintendo 64 Discord](https://discord.gg/jqPzxUVVMJ) - The /r/n64 community server for Nintendo 64 enthusiasts

## Documentation

* [cen64#58](https://github.com/n64dev/cen64/issues/58) ⭐ 842 | 🐛 64 | 🌐 C | 📅 2025-10-26 - A cen64 issue comment summarizing the boot process
* [RSP](https://github.com/rasky/r64emu/blob/master/doc/rsp.md) ⭐ 177 | 🐛 6 | 🌐 Rust | 📅 2022-11-02 - Detailed RSP documentation in the r64emu emulator repository
* [Accessory Reference](http://github.com/joeldipops/TransferBoy/blob/master/docs/TransferPakReference.md) ⭐ 50 | 🐛 20 | 🌐 C | 📅 2020-11-12 - Guide on how to communicate with the Transfer Pak and Rumble Pak
* [64DD wiki](https://github.com/LuigiBlood/64dd/wiki) ⭐ 48 | 🐛 0 | 🌐 C | 📅 2020-08-11 - Documentation on 64DD hardware, disks, and related cartridges
* [64DD-schematics](https://github.com/ChrisPVille/64dd-schematics) ⭐ 25 | 🐛 0 | 📅 2020-08-20 - Schematics for the Nintendo 64 Disk Drive (N64DD)
* [Ultra64](https://ultra64.ca/) - An absolute wealth of documentation including official development manuals, as well as SDK downloads and reference material
* [Nintendo 64 Architecture](https://copetti.org/projects/consoles/nintendo-64/) - An overview of the console architecture
* [N64brew Wiki](https://n64brew.dev/) - The N64brew community wiki
* [N64dev](http://n64dev.org/) - Useful N64 hacking links
* [NEC VR4300 CPU Manual @ N64dev](http://n64dev.org/p/U10504EJ7V0UMJ1.pdf) - The manual for the NEC VR4300 CPU used by the Nintendo 64
* [Console Protocols](https://sites.google.com/site/consoleprotocols/home) - Nintendo 64 hardware info, memory map, PIF boot stage reference, and JoyBus I/O documentation
* [dragonminded N64DEV](https://dragonminded.com/n64dev/) - `libdragon` usage, Windows and Linux toolchains, and RCP documentation
* [N64 ROM Formats](http://n64dev.org/romformats.html) - A short N64 ROM format quick reference sheet
* [N64 ROM Formats Explained](https://www.reddit.com/r/emulation/comments/7hrvzp/the_three_different_n64_rom_formats_explained_for/?st=jn9t30t4\&sh=1951de19) - Details the three commonly encountered Nintendo 64 ROM formats (use Big Endian/.z64)
* [Hack64](https://hack64.net/wiki/doku.php?id=nintendo_64) - A variety of documentation on RCP data structures, compression, assembly, and more
* [64dd.org](https://64dd.org) - Nintendo 64DD documentation, emulators, homebrew, and tools
* [Microcode from source](https://olivieryuyu.blogspot.com/2019/11/how-to-compile-n64-microcode-from-source.html) - How to compile microcode from source
* [N64 cartridge info](https://n64brew.dev/wiki/Game_Pak) - Cartridge pinout

## Videos

* [Installing the Nintendo 64 Development Kit](https://www.youtube.com/watch?v=84wk0mZ8gfM) - How to install the Nintendo 64 Software Development Kit under Windows 2000 and 98SE and build sample code. Also generally works under Windows XP.
* [Behind The Code](https://www.youtube.com/c/BehindTheCode001/videos) - Gerry O'Brien's YouTube channel, with a number of videos discussing Nintendo 64 development with NuSystem and the official SDK, development hardware, audio processing, and more
* [Building cen64 for Speed and Preservation](https://www.youtube.com/watch?v=lvr6-6U0ck8) - Tyler Stachecki and Mike Ryan discuss making the cen64 emulator fast without compromising on accuracy
* [REcon 2015 - Reversing the Nintendo 64 CIC](https://www.youtube.com/watch?v=HwEdqAb2l50) - Mike Ryan, MarshallH, and John McMaster talk about reverse engineering and cloning a 20 year old copy protection chip (the N64 CIC)
* [Portland Retro Gaming Expo 2019 - N64 Homebrew Development - Part 1](https://www.youtube.com/watch?v=zpDkENNnrZk) - Victor Vieux talks about the Nintendo 64 technical specifications and begins building a game using `libdragon`
* [Portland Retro Gaming Expo 2019 - N64 Homebrew Development - Part 2](https://www.youtube.com/watch?v=V9y-2LiJsI0) - Victor Vieux adds sound and graphic assets and talks about the future of Nintendo 64 homebrew development
* [Programming for Nintendo 64](https://www.youtube.com/watch?v=aKXEooIPwP0) - Damjan Nesic goes through the basics of programming for Nintendo 64 using C and a Windows XP virtual machine
* [Reflective Regret: Adventures in N64 Development](https://www.youtube.com/watch?v=ZgPWE0Wkg7g) - Buu342's seminar on Nintendo 64 homebrew game development at Inércia Demoparty 2021 (with [code available](https://github.com/buu342/N64-ReflectiveRegretPresentation) ⭐ 18 | 🐛 0 | 🌐 C | 📅 2022-01-23)
* [Debugging N64 homebrew using GDB with a flashcart](https://www.youtube.com/watch?v=Fr8rSqsFuWk) - Buu342 demonstrates how to use UNFLoader with GDB to debug Libultra, ModernSDK, and Libdragon homebrew running on a flashcart

## Toolchains

* [n64chain](https://github.com/tj90241/n64chain) ⭐ 156 | 🐛 11 | 🌐 C | 📅 2022-10-07 - A development toolchain based on GCC that does not depend on any proprietary Nintendo library
* [glankk/n64](https://github.com/glankk/n64) ⭐ 115 | 🐛 4 | 🌐 C | 📅 2026-06-16 - A collection of files and tools used to compile and test code for the Nintendo 64
* [n64sdkmod](https://github.com/CrashOveride95/n64sdkmod) ⭐ 101 | 🐛 0 | 🌐 C | 📅 2024-01-12 - A `libultra` SDK for the modern era, supported on Debian-based Linux distros
* [modern-n64sdk](https://github.com/trhodeos/modern-n64sdk) ⭐ 55 | 🐛 1 | 📅 2018-10-16 - Describes how to get a modern build of GCC cross-compiling on a modern OS (Linux, Windows, macOS)
* [libdragon-docker](https://github.com/anacierdem/libdragon-docker) ⭐ 38 | 🐛 12 | 🌐 JavaScript | 📅 2026-03-06 - Dockerized toolchain based on [libdragon](https://github.com/DragonMinded/libdragon) ⭐ 1,232 | 🐛 95 | 🌐 C | 📅 2026-09-01
* [mips64-gcc-toolchain](https://github.com/N64-tools/mips64-gcc-toolchain) ⚠️ Archived - Windows and Linux scripts to automate building of a modern MIPS64 GCC toolchain for Nintendo 64 cross compilation
* [portable-n64-toolchain](https://github.com/Mr-Pnut/portable-n64-toolchain) ⭐ 16 | 🐛 2 | 🌐 Shell | 📅 2019-01-25 - A Dockerized toolchain based on modern-n64sdk
* [homebrew-n64-dev](https://github.com/tehzz/homebrew-n64-dev) ⭐ 6 | 🐛 4 | 🌐 Ruby | 📅 2021-12-29 - macOS `gcc` and `binutils` [Homebrew](https://brew.sh) formulae for Nintendo 64 development
* [Official Nintendo 64 SDKs](https://ultra64.ca/resources/software/) - Official Nintendo 64 Software Development Kits for Windows and SGI IRIX
* [N64 SDK Easy Install CD](https://mega.nz/#!AOYDkSxA!MuAqt8iRBk0GGbaqaXVYB9tfZxsquKg5QkbCRL3VOLM) - An ISO image made by AlphaTango and CrashOveride to simplify installation of the official SDK. Works on Windows 98-XP.

## Assemblers

* [armips](https://github.com/Kingcom/armips) ⭐ 411 | 🐛 31 | 🌐 C++ | 📅 2026-08-01 - An assembler for various ARM and MIPS platforms
* [naken\_asm](https://github.com/mikeakohn/naken_asm) ⭐ 340 | 🐛 14 | 🌐 C++ | 📅 2026-05-30 - An assembler for a variety of CPUs including standard MIPS III (Nintendo 64 CPU) and RSP
* [ARM9/bass](https://github.com/ARM9/bass) ⭐ 194 | 🐛 14 | 🌐 C++ | 📅 2023-07-29 - A fork of byuu's bass assembler which has been updated with Nintendo 64 MIPS/RSP/RDP output
* [lips](https://github.com/notwa/lips) ⭐ 19 | 🐛 0 | 🌐 Lua | 📅 2018-04-28 - A MIPS R4300i assembler written in Lua
* [Screwaround64](https://github.com/superjack111/screwaround64) ⭐ 9 | 🐛 0 | 🌐 C | 📅 2019-04-02 - An interactive assembler for Nintendo 64

## Emulators

### Actively Maintained

* [Project64](https://www.pj64-emu.com) ([GitHub](https://github.com/project64/project64) ⭐ 3,030 | 🐛 275 | 🌐 C++ | 📅 2026-08-30) - An open-source emulator for Windows and (soonTM) Linux/Android. It used to focus on compatibility with commercial games, but now also focuses on improving accuracy and emulating as much of the console as possible while remaining performant and compatible.
* [simple64](https://simple64.github.io/) ([GitHub](https://github.com/simple64/simple64) ⚠️ Archived) - A fork of Mupen64Plus that is easy to use and also more accurate.
* [Rosalie's Mupen GUI](https://github.com/Rosalie241/RMG) ⭐ 1,098 | 🐛 136 | 🌐 C++ | 📅 2026-07-29 - a GUI for Mupen64Plus that works on Windows. One of the easiest and best ways to use Mupen64Plus with a GUI!
* [Dillonb's dgb-n64](https://github.com/Dillonb/n64) ⭐ 185 | 🐛 8 | 🌐 C++ | 📅 2026-08-31 - A low-level, accurate N64 emulator for Windows and Linux. It includes a CPU recompiler, and emulates RDP with Vulkan (via parallel-RDP).
* [ModLoader64](https://modloader64.com) ([GitHub](https://github.com/hylian-modding/ModLoader64) ⭐ 71 | 🐛 7 | 🌐 TypeScript | 📅 2023-03-06) - A wrapper for Mupen64plus that enables modding through plugins written in TypeScript
* [Sixtyforce](https://sixtyforce.com) - A closed-source emulator for Mac
* [mupen64plus](https://mupen64plus.org) ([GitHub](https://github.com/mupen64plus)) - A more recently updated fork of Mupen64 for Linux, Mac OSX, FreeBSD, and Windows. No GUI is included, so you can use simple64, RMG, or the RetroArch core for a UI.
* [Mupen64+ Reverser Edition](https://www.retroreversing.com/mupen64RE) - A fork of the Mupen64Plus emulator tailored for reverse engineering.
* [ares](https://ares-emu.net) - A low-level, accurate multi-system emulator with good support for N64. Available in sources and binary distributions for Windows, Mac and Linux. It includes a CPU and RSP recompiler, and emulates RDP with Vulkan (via Parallel-RDP).

### Works In Progress

* [Gopher64](https://github.com/gopher64/gopher64) ⭐ 1,236 | 🐛 16 | 🌐 Rust | 📅 2026-08-30 - An N64 emulator written in Rust by the developer of Simple64, able to already play some commercial games at decent speeds!
* [cor64](https://github.com/bryanperris/cor64) ⭐ 53 | 🐛 9 | 🌐 C# | 📅 2024-02-14 - An in-progress emulator written in C#
* [Kaizen (previously Gadolinium)](https://github.com/mehmetpeker1/Kaizen) ⭐ 0 | 🐛 0 | 📅 2024-01-30 - Work-in-progress emulator written in C++, able to already play some commercial games and replay Mupen TAS movies

### Unmaintained

* [cen64](https://github.com/n64dev/cen64) ⭐ 842 | 🐛 64 | 🌐 C | 📅 2025-10-26 - A [cycle-accurate](https://retrocomputing.stackexchange.com/questions/1191/what-exactly-is-a-cycle-accurate-emulator) emulator for Windows, Linux, and Mac. While currently not fast enough to play games at full speed, it aims for perfect emulation by emulating the hardware inside of the console down to the register-transfer level. Widely used to test ROMs in lieu of or before using real hardware.
* [Not64](https://github.com/extremscorner/not64) ⭐ 370 | 🐛 1 | 🌐 C | 📅 2026-04-10 - A fork of Wii64
* [r64emu](https://github.com/rasky/r64emu) ⭐ 177 | 🐛 6 | 🌐 Rust | 📅 2022-11-02 - A N64 low-level emulator written in Rust
* [1964](http://1964emu.emulation64.com) - An open-source emulator for Windows
* [mupen64](http://mupen64.emulation64.com) - An open-source, multi-platform emulator
* [Wii64](https://wiibrew.org/wiki/Wii64) - A port of mupen64 for Nintendo Wii and GameCube
* [Mupen64-360](https://gbatemp.net/download/mupen64-360_v0-993_beta2.34126) - A port of Wii64 (and thus mupen64) to the Xbox 360. No longer maintained.
* Project Unreality - An early emulator for Windows
* [Nemu64](http://www.emulation64.com/files/info/202/nemu64.html/) - A closed-source emulator for Windows with fantastic debugging tools. Currently is incredibly difficult to run on modern Windows.
* [UltraHLE](https://en.wikipedia.org/wiki/UltraHLE) - An early emulator for Windows. Though closed-source, [the source leaked in 2002](https://web.archive.org/web/20020812020546/http://www.emulation64.com/freeflow-page.html).
* [Surreal64](http://surreal64.sourceforge.net) and [Surreal64 CE](http://surreal64ce.wikidot.com) - An emulator for the original Xbox which includes ports of 1964, Project64, and UltraHLE
* [TrueReality](https://sourceforge.net/projects/truereality/) - An open-source emulator

## Development Hardware

* [N64cart](https://github.com/pdaxrom/N64cart) ⭐ 78 | 🐛 10 | 🌐 C | 📅 2026-06-13 - A flash cartridge based on the RP2040 microcontroller
* [Brutzelkarte](https://github.com/jago85/Brutzelkarte_PCB) ⭐ 66 | 🐛 1 | 📅 2020-05-19 - An open-source (hardware and software) FPGA-based flash cartridge
* [gs\_libusb](https://github.com/hcs64/gs_libusb) ⭐ 39 | 🐛 3 | 🌐 C | 📅 2014-10-10 - GameShark Pro utilities using libusb over a USB parallel port adapter
* [El Barato 64](https://github.com/Hazematman/El-Barato-64) ⭐ 24 | 🐛 5 | 🌐 C | 📅 2020-08-11 - An in-progress open source development cartridge
* [SummerCart64](https://summercart64.dev) - A fully open source, production ready, flashcart with 64DD implementation built-in. Mostly geared towards homebrew development.
* [EverDrive 64 X7](https://krikzz.com/store/home/55-everdrive-64-x7.html) - A flash cartridge with USB support for development
* [64drive](http://64drive.retroactive.be/) - A flash cartridge with USB support targeted at developers. Currently near impossible to get new, or expensive second hand.
* [UltraHDMI](http://ultrahdmi.retroactive.be/) (periodically in stock at [Game-Tech](https://www.game-tech.us/product/ultrahdmi/)) - A board that can be installed into the console to capture the digital output of the RCP and send it out a Mini HDMI connector to a modern TV. Convenient for connecting a real console to a nearby monitor while viewing the best possible output signal.
* [N64RGB](https://etim.net.au/shop/shop.php?crn=209\&rn=548\&action=show_detail) - An N64RGB mod that supports every motherboard revision and works pretty well.
* [UltraSave](http://64drive.retroactive.be/features.php#ultrasave) - A device that works with the 64drive to transfer saves from real cartridges
* [GameShark 3.0+](https://hackaday.com/2019/01/11/nintendo-64-homebrew-via-game-shark/) - A method of running homebrew via a GameShark
* [sm64gameshark](https://sites.google.com/site/sm64gameshark/resources/transfering-codes-over-usb) - How to transfer GameShark codes from USB to parallel, and how to identify GameShark cartridges with functional parallel ports
* [Replacement Carts](https://n64preservationproject.com/) - A set of EagleCAD files for manufacturing your own N64 carts
* [ED64 Plus](https://ed64p.com/) - A Chinese clone of the Everdrive 64 at a much cheaper price point. It also has a disconnected USB port with a missing FT245R chip that [can be reattached](https://odysee.com/@backofficeshow:f/everdrive-ed64-nintendo-64-teardown:0) for theoretical added functionality.

## Tools and Libraries

### Development Cartridge Loaders

* [sc64deployer](https://github.com/Polprzewodnikowy/SummerCart64/releases) ⭐ 1,137 | 🐛 16 | 🌐 C | 📅 2025-05-11 - SummerCart64 loader and control software (Windows, macOS and Linux)
* [UNFLoader](https://github.com/buu342/N64-UNFLoader/) ⭐ 133 | 🐛 13 | 🌐 C++ | 📅 2026-05-15 - A universal flash cart ROM uploader (64drive, EverDrive 64 V3, EverDrive 64 X7 and SummerCart64) and debug library
* [ed64](https://github.com/anacierdem/ed64) ⭐ 30 | 🐛 14 | 🌐 JavaScript | 📅 2023-12-20 - Tools to develop on an EverDrive 64 cartridge
* [g64drive](https://github.com/rasky/g64drive) ⭐ 29 | 🐛 4 | 🌐 Go | 📅 2025-06-09 - Linux/Mac tool for operating a 64drive development cartridge
* [loader64](https://github.com/jsdf/loader64) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2020-04-05 - A USB uploader for EverDrive 64

### Flashcart Menu Software

* [N64FlashcartMenu](https://github.com/Polprzewodnikowy/N64FlashcartMenu) ⭐ 457 | 🐛 45 | 🌐 C | 📅 2026-08-31 - Universal flashcart menu with aim to support most of the N64 flashcarts on the market

### Asset Conversion and Viewing

#### 3D

* [Fast64](https://github.com/Fast-64/fast64) ⭐ 532 | 🐛 77 | 🌐 Python | 📅 2026-08-31 - A Blender plugin to preview and export meshes as F3D display lists for decomp and homebrew projects.
* [Sausage64](https://github.com/buu342/Blender-Sausage64) ⭐ 90 | 🐛 4 | 🌐 C | 📅 2026-01-18 - A Blender plugin to export "sausage link" style character models with animations
* [objn64](https://github.com/n64dev/objn64) ⭐ 25 | 🐛 0 | 🌐 C | 📅 2014-12-20 - Wavefront `.obj` model converter that generates optimized displaylists for compilation with `libultra`
* [Blen64](https://github.com/GCaldL/Blen64) ⭐ 20 | 🐛 0 | 🌐 Python | 📅 2019-01-23 - Blender scripts to export meshes to draw lists as header files
* [N64\_3DRenderingTest](https://github.com/tfcat/N64_3DRenderingTest) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2018-07-17 - A basic model viewer using NuSystem
* [Obj2N64DL](https://github.com/pseudophpt/Obj2N64DL) ⭐ 10 | 🐛 1 | 🌐 C# | 📅 2017-10-02 - Another Wavefront `.obj` to displaylist converter
* [blend2niff](https://github.com/1r3n33/blend2niff) ⭐ 7 | 🐛 2 | 🌐 Python | 📅 2020-11-10 - A Blender add-on to export to [NIFF2](http://n64devkit.square7.ch/niff/index.htm) (Nintendo Intermediate File Format 2)
* [Blender64](https://github.com/engerb/Blender64) ⭐ 6 | 🐛 0 | 🌐 Python | 📅 2020-06-24 - A Python tool to export Blender 3D models to F3DEX2 microcode display lists
* [Max\_To\_N64](https://github.com/MrQuetch/Max_To_N64) ⭐ 4 | 🐛 0 | 🌐 MAXScript | 📅 2021-10-18 - Scripts to export models from 3DS Max to C
* [64Drive Viewer](https://www.youtube.com/watch?v=yUX1Vga6amg) - Preview textures, images, sounds, and 3D models on hardware with a 64drive over USB

#### 2D

* [Texture64](https://github.com/queueRAM/Texture64) ⭐ 101 | 🐛 6 | 🌐 C# | 📅 2021-01-02 - A texture ripper and editor with support for multiple formats
* [n64rawgfx](https://github.com/Octocontrabass/n64rawgfx) ⭐ 25 | 🐛 0 | 🌐 C | 📅 2013-11-22 - A tool to export and import uncompressed/raw graphics from ROMs
* [GML-N64TextureConverter](https://github.com/buu342/GML-N64TextureConverter) ⭐ 23 | 🐛 6 | 🌐 Game Maker Language | 📅 2022-11-07 - Converts standard image formats to Nintendo 64 compatible C header files
* [N64GFXCookie](https://github.com/LuigiBlood/N64GFXCookie) ⭐ 10 | 🐛 0 | 🌐 C# | 📅 2020-04-13 - Nintendo 64 CI8 format graphics viewer/editor
* [mksprite2](https://github.com/farisawan-2000/mksprite2) ⭐ 8 | 🐛 0 | 🌐 Python | 📅 2021-06-14 - A Python 3 script to create sprite and background objects for use with S2DEX microcode
* [n64texconv](https://github.com/coleferg/n64texconv) ⭐ 7 | 🐛 0 | 🌐 Python | 📅 2020-10-24 - A Python tool to convert PNG to RGBA(16/32), CI(4/8), and I(A)(4/8)
* [n64CIconverter](https://github.com/darklink623/n64CIconverter) ⭐ 7 | 🐛 0 | 🌐 C# | 📅 2019-04-29 - Converts standard image formats to Nintendo 64's [Color Index (CI) format](https://n64squid.com/homebrew/n64-sdk/textures/image-formats/#CI)
* [mkspriten64](https://github.com/nathanduma/mkspriten64) ⭐ 5 | 🐛 0 | 🌐 C++ | 📅 2020-06-16 - Windows equivalent to the SGI program `mksprite`. Converts .png to a .h header and .c source file.
* [png2n64](https://github.com/matthieularere/png2n64) ⭐ 3 | 🐛 0 | 🌐 Python | 📅 2020-06-11 - A Python 3 script to convert PNG images to 16 bit RBGA
* [png2c](https://github.com/selfVSmind/png2c) ⭐ 2 | 🐛 0 | 🌐 C++ | 📅 2020-11-09 - A C++ command line tool to convert PNG images to `libultra`-compatible texture header files
* [ImageMerge](https://github.com/TheRDavid/ImageMerge) ⭐ 2 | 🐛 0 | 🌐 Java | 📅 2017-01-11 - Converts two 8-bit images into 2-bit images and packs them into 1 image to save space in a ROM
* [Spritemapper](https://github.com/TheRDavid/Spritemapper) ⭐ 2 | 🐛 0 | 🌐 Java | 📅 2017-02-20 - Arranges a directory of equally-sized images into a sprite map and compresses it
* [xo-tt64](https://github.com/xoorath/xo-tt64) ⚠️ Archived - Converts input images to .c files of the same name

### Audio Playback and Editing

* [N64-Tools](https://github.com/jombo23/N64-Tools/tree/master/N64MidiTool) ⭐ 333 | 🐛 39 | 🌐 C++ | 📅 2026-07-26 - A tool to extract and import audio from many games that make use of the MIDI format
* [seq64](https://github.com/sauraen/seq64) ⭐ 166 | 🐛 7 | 🌐 C++ | 📅 2025-10-26 - A full-featured editor for sequenced music in first-party games
* [ANMP](https://github.com/derselbst/ANMP) ⭐ 41 | 🐛 7 | 🌐 C++ | 📅 2026-04-28 - A multi-channel loopable video game music player, with support for various Nintendo 64 audio formats
* [sfz2n64](https://github.com/lambertjamesd/sfz2n64) ⭐ 14 | 🐛 0 | 🌐 Go | 📅 2026-03-19 - Converts SFZ files to a format the Nintendo 64 can use as part of instrument banks
* [N64-SoundTester](https://github.com/buu342/N64-SoundTester) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2020-05-28 - A ROM that allows you to test out N64 Sound Tools sample banks and tune them directly on your console or emulator, avoiding lengthy turnaround times
* [ultra\_mpeg](https://github.com/devwizard64/ultra_mpeg/) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2022-05-08 - An MPEG-1/2 decoder library
* [libmad-n64](https://github.com/parasyte/libmad-n64) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2014-06-29 - [libmad](https://www.underbit.com/products/mad/) with MIPS patches, for MPEG audio playback
* [midicvt](https://github.com/lambertjamesd/midicvt) ⭐ 6 | 🐛 0 | 🌐 Go | 📅 2022-03-15 - An open source replacement for `midicvt` to create MIDI files compatible with `libultra`

### Debugging

* [n64rd](https://github.com/parasyte/n64rd) ⭐ 34 | 🐛 4 | 🌐 C | 📅 2017-09-25 - Remote debugger for GameShark 3.2 hardware over a parallel interface
* [ed64log](https://github.com/jsdf/ed64log) ⭐ 19 | 🐛 0 | 🌐 C | 📅 2023-07-30 - A tool and [example code](https://github.com/jsdf/ed64log/tree/master/example#exception-logging-and-disassembly) ⭐ 19 | 🐛 0 | 🌐 C | 📅 2023-07-30 to implement development logging from a homebrew ROM running on an EverDrive 64
* [gdbstub-ed64](https://github.com/murachue/gdbstub-ed64) ⭐ 17 | 🐛 2 | 🌐 C | 📅 2020-04-04 - Another EverDrive 64 GDB stub
* [Project64 EmuScripts](https://github.com/LuigiBlood/EmuScripts/tree/master/N64/Project64) ⭐ 16 | 🐛 1 | 🌐 JavaScript | 📅 2026-07-01 - Scripts for debugging under Project64 emulation
* [N64-GDB-stub](https://github.com/Hazematman/N64-GDB-stub) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2020-08-22 - A GDB stub that works with a modified version of the cen64 emulator
* [webserial-ed64log](https://github.com/jsdf/webserial-ed64log) ⭐ 6 | 🐛 0 | 🌐 JavaScript | 📅 2020-07-18 - An ed64log client using Web Serial API
* [ed64-gdb](https://github.com/networkfusion/ed64-gdb) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2019-05-09 - A GDB stub for debugging with an EverDrive 64 V3

### ROM Manipulation

* [splat](https://github.com/ethteck/splat) ⭐ 352 | 🐛 42 | 🌐 Python | 📅 2026-07-27 - A ROM splitting tool to assist with decompilation and modding projects
* [boot\_stub](https://github.com/hcs64/boot_stub) ⭐ 37 | 🐛 0 | 🌐 Assembly | 📅 2022-10-06 - A replacement for the CIC-6102 IPL3 boot code
* [rom64](https://github.com/mroach/rom64) ⭐ 34 | 🐛 3 | 🌐 Go | 📅 2023-12-15 - A tool to identify and parse ROM header information
* [spicy](https://github.com/trhodeos/spicy) ⭐ 25 | 🐛 3 | 🌐 Go | 📅 2022-10-14 - An open-source replacement of the official SDK's `mild.exe` (referenced by `$(MAKEROM)` in many Makefiles). Packs object files into an N64-compatible ROM.
* [leotools](https://github.com/jkbenaim/leotools) ⭐ 20 | 🐛 0 | 🌐 C | 📅 2016-07-25 - Work with 64DD disk images and the files contained therein
* [makemask](https://github.com/trhodeos/makemask) ⭐ 14 | 🐛 0 | 🌐 Go | 📅 2022-10-14 - An open-source replacement of the official SDK's `makemask.exe`. Adds a mask to a compiled ROM which pads the file to fill the entire cartridge space, adds a CIC version, and adds informational headers to the file. Typically run immediately after `mild.exe`. More on this tool at [N64Squid](https://n64squid.com/homebrew/n64-sdk/software/mipse-ultra-gcc/makemask/).
* [romjudge](https://github.com/jkbenaim/romjudge) ⭐ 13 | 🐛 2 | 🌐 C | 📅 2023-06-07 - A utility to judge an N64 ROM for correctness
* [ipl3hasher](https://github.com/awygle/ipl3hasher) ⭐ 11 | 🐛 9 | 🌐 Rust | 📅 2020-07-18 - GPU-accelerated hash collision finder for the IPL3 boot code
* [makeromOpen](https://github.com/fraser125/makeromOpen) ⭐ 3 | 🐛 0 | 🌐 Assembly | 📅 2020-01-17 - Another open-source makerom replacement (work in progress)
* [N64ShellPreview](https://github.com/Random06457/N64ShellPreview) ⭐ 2 | 🐛 0 | 🌐 C# | 📅 2020-07-03 - A Windows Shell Extension to display ROM information in Explorer's preview pane
* [Tool N64](https://www.zophar.net/utilities/n64aud/tool-n64.html) - A tool to display ROM information and perform byte reordering
* [Real N64 CRC Tool v2](https://www.smwcentral.net/?p=section\&a=details\&id=8799) - A tool to check, calculate, and set ROM checksums and extract the bootcode of ROM files
* [Info64](https://www.smwcentral.net/?p=section\&a=details\&id=5737) - A tool to display and set ROM header information and checksums

### Development Libraries

* [libdragon](https://github.com/DragonMinded/libdragon) ⭐ 1,232 | 🐛 95 | 🌐 C | 📅 2026-09-01 - An open-source library for Nintendo 64 development
* [tiny3d](https://github.com/HailToDodongo/tiny3d) ⭐ 561 | 🐛 3 | 🌐 C++ | 📅 2026-08-30 - A tiny 3D RSP microcode and C API wrapper which work with `libdragon`
* [libreultra](https://github.com/n64decomp/libreultra) ⭐ 182 | 🐛 2 | 🌐 C | 📅 2022-01-29 - A decompilation of the Nintendo 64 standard SDK library, `libultra`
* [libn64](https://github.com/tj90241/n64chain/tree/master/libn64) ⭐ 156 | 🐛 11 | 🌐 C | 📅 2022-10-07 - An open-source library for Nintendo 64 development, part of `n64chain`
* [pseultra](https://github.com/pseudophpt/pseultra) ⭐ 78 | 🐛 4 | 🌐 C | 📅 2019-09-09 - A collection of tools used to develop software for the Nintendo 64 that are distinct from the official SDK
* [ultralib](https://github.com/decompals/ultralib) ⭐ 67 | 🐛 11 | 🌐 C | 📅 2026-04-19 - A reverse engineering of `libultra`
* [framework64](https://github.com/matthewcpp/framework64) ⭐ 26 | 🐛 1 | 🌐 C | 📅 2026-08-30 - An asset pipeline and C library to simplify game creation (uses n64sdkmod)
* [libhfx](https://github.com/Hazematman/libhfx) ⭐ 19 | 🐛 0 | 🌐 C | 📅 2021-09-19 - An in-progress open source library for 3D graphics
* [S2DEX Text Engine](https://github.com/someone2639/S2DEX-Text-Engine) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2025-07-20 - A text engine powered by the S2DEX microcode
* [n64ut](https://github.com/n64ut) - An in-progress set of modern Nintendo 64 libraries

## Reverse Engineering

### Projects

#### Game Decompilation

* [Super Mario 64](https://github.com/n64decomp/sm64) ⭐ 8,749 | 🐛 28 | 🌐 C | 📅 2024-02-04 - A **complete** decompilation of *Super Mario 64*
* [The Legend of Zelda: Ocarina of Time](https://github.com/zeldaret/oot) ⭐ 5,494 | 🐛 75 | 🌐 C | 📅 2026-09-01 - A **complete** decompilation of *The Legend of Zelda: Ocarina of Time*
* [The Legend of Zelda: Majora's Mask](https://github.com/zeldaret/mm) ⭐ 1,712 | 🐛 11 | 🌐 C | 📅 2026-08-30 - A **complete** decompilation of *The Legend of Zelda: Majora's Mask*
* [Paper Mario](https://github.com/pmret/papermario) ⭐ 1,604 | 🐛 34 | 🌐 C | 📅 2026-08-25 - A **complete** decompilation of *Paper Mario*
* [Mario Kart 64](https://github.com/n64decomp/mk64) ⭐ 1,294 | 🐛 35 | 🌐 C | 📅 2026-08-16 - A **complete** decompilation of *Mario Kart 64*
* [Diddy Kong Racing](https://github.com/DavidSM64/Diddy-Kong-Racing) ⭐ 420 | 🐛 4 | 🌐 C | 📅 2026-08-18 - An in-progress decompilation of *Diddy Kong Racing*
* [Dōbutsu no Mori](https://github.com/zeldaret/af) ⭐ 291 | 🐛 6 | 🌐 C | 📅 2026-08-16 - An in-progress decompilation of *Dōbutsu no Mori*
* [Duke Nukem: Zero Hour](https://github.com/gillou68310/dukenukemzerohour) ⭐ 271 | 🐛 0 | 🌐 C | 📅 2025-11-06 - A **complete** decompilation of *Duke Nukem: Zero Hour*
* [Super Smash Bros.](https://github.com/vetritheretri/ssb-decomp-re) ⭐ 245 | 🐛 3 | 🌐 C | 📅 2026-08-25 - An in-progress decompilation of *Super Smash Bros.*
* [Conker's Bad Fur Day](https://github.com/mkst/conker) ⚠️ Archived - An in-progress decompilation of *Conker's Bad Fur Day*
* [Doom 64](https://github.com/Erick194/DOOM64-RE) ⭐ 236 | 🐛 1 | 🌐 C | 📅 2025-05-30 - A **complete** decompilation of *Doom 64*
* [Kirby 64: The Crystal Shards](https://github.com/kirby64ret/kirby64) ⭐ 228 | 🐛 3 | 🌐 Assembly | 📅 2026-08-30 - An in-progress decompilation of *Kirby 64: The Crystal Shards*
* [Harvest Moon 64](https://github.com/harvestwhisperer/hm64-decomp) ⭐ 217 | 🐛 2 | 🌐 C | 📅 2026-07-02 - An in-progress decompilation of *Harvest Moon 64*
* [Dinosaur Planet](https://github.com/zestydevy/dinosaur-planet) ⭐ 216 | 🐛 1 | 🌐 C | 📅 2026-09-01 - An in-progress decompilation of *Dinosaur Planet*
* [Pokémon Stadium](https://github.com/pret/pokestadium) ⭐ 198 | 🐛 6 | 🌐 C | 📅 2026-09-01 - An in-progress decompilation of *Pokémon Stadium*
* [Snowboard Kids 2](https://github.com/cdlewis/snowboardkids2-decomp) ⭐ 187 | 🐛 4 | 🌐 C | 📅 2026-08-30 - An in-progress decompilation of *Snowboard Kids 2*
* [Banjo-Tooie](https://github.com/mr-wiseguy/banjo-tooie) ⭐ 137 | 🐛 5 | 🌐 C | 📅 2025-11-29 - An in-progress decompilation of *Banjo-Tooie*
* [Wave Race 64](https://github.com/LLONSIT/wave-race-64) ⭐ 104 | 🐛 3 | 🌐 Assembly | 📅 2026-08-31 - An in-progress decompilation of *Wave Race 64*
* [F-Zero X](https://github.com/inspectredc/fzerox) ⭐ 102 | 🐛 2 | 🌐 C | 📅 2026-08-31 - An in-progress decompilation of *F-Zero X*
* [Pokémon Snap](https://github.com/ethteck/pokemonsnap) ⭐ 100 | 🐛 7 | 🌐 C | 📅 2026-08-29 - An in-progress decompilation of *Pokémon Snap*
* [Yoshi's Story](https://github.com/decompals/yoshis-story) ⭐ 78 | 🐛 1 | 🌐 C | 📅 2026-04-19 - An in-progress decompilation of *Yoshi's Story*
* [Dr. Mario 64](https://github.com/angheloalf/drmario64) ⭐ 76 | 🐛 0 | 🌐 C | 📅 2026-08-13 - An in-progress decompilation of *Dr. Mario 64*
* [Mario Party](https://github.com/mariopartyrd/marioparty) ⭐ 76 | 🐛 1 | 🌐 C | 📅 2026-06-28 - An in-progress decompilation of *Mario Party*
* [Mischief Makers](https://github.com/drahsid/mischief-makers) ⭐ 71 | 🐛 3 | 🌐 C | 📅 2026-08-16 - An in-progress decompilation of *Mischief Makers*
* [Mario Party 3](https://github.com/mariopartyrd/marioparty3) ⭐ 66 | 🐛 0 | 🌐 C | 📅 2026-09-01 - An in-progress decompilation of *Mario Party 3*
* [Space Station Silicon Valley](https://github.com/mkst/sssv) ⭐ 64 | 🐛 0 | 🌐 C | 📅 2026-08-31 - An in-progress decompilation of *Space Station Silicon Valley*
* [Bomberman Hero](https://github.com/bomberhackers/bmhero) ⭐ 60 | 🐛 0 | 🌐 C | 📅 2026-04-24 - An in-progress decompilation of *Bomberman Hero*
* [Castlevania 64](https://github.com/k64ret/cv64) ⭐ 56 | 🐛 5 | 🌐 C | 📅 2026-07-28 - An in-progress decompilation of *Castlevania 64*
* [Jet Force Gemini](https://github.com/ryan-myers/jet-force-gemini) ⭐ 52 | 🐛 2 | 🌐 C | 📅 2026-09-01 - An in-progress decompilation of *Jet Force Gemini*
* [Mario Party 2](https://github.com/mariopartyrd/marioparty2) ⭐ 51 | 🐛 0 | 🌐 C | 📅 2026-04-26 - An in-progress decompilation of *Mario Party 2*
* [Pokémon Stadium 2](https://github.com/pret/pokestadiumgs) ⭐ 49 | 🐛 0 | 🌐 C | 📅 2026-07-10 - An in-progress decompilation of *Pokémon Stadium 2*
* [Rocket: Robot on Wheels](https://github.com/RocketRet/Rocket-Robot-On-Wheels) ⭐ 46 | 🐛 4 | 🌐 C | 📅 2023-01-15 - An in-progress decompilation of *Rocket: Robot on Wheels*
* [Blast Corps](https://github.com/retroplastic/blastcorps) ⭐ 40 | 🐛 1 | 🌐 C | 📅 2021-12-28 - An in-progress decompilation of *Blast Corps*
* [Aidyn Chronicles](https://github.com/blackgamma7/Aidyn) ⭐ 39 | 🐛 0 | 🌐 C++ | 📅 2026-09-01 - An in-progress decompilation of *Aidyn Chronicles*
* [Body Harvest](https://github.com/jaytheham/body-harvest-decompilation) ⭐ 39 | 🐛 2 | 🌐 C | 📅 2026-09-01 - An in-progress decompilation of *Body Harvest* in D (see also [DeltaniumIndustries/BodyHarvestDecomp](https://github.com/DeltaniumIndustries/BodyHarvestDecomp) ⚠️ Archived)
* [Neon Genesis Evangelion 64](https://github.com/farisawan-2000/evangelion) ⭐ 36 | 🐛 2 | 🌐 C | 📅 2025-07-13 - An in-progress decompilation of *Neon Genesis Evangelion 64*
* [Pokémon Puzzle League](https://github.com/angheloalf/puzzleleague64) ⭐ 35 | 🐛 1 | 🌐 C | 📅 2026-09-01 - An in-progress decompilation of *Pokémon Puzzle League*
* [Bomberman 64](https://github.com/bomberhackers/bm64) ⭐ 33 | 🐛 0 | 🌐 C | 📅 2026-03-08 - An in-progress decompilation of *Bomberman 64*
* [AeroGauge](https://github.com/LLONSIT/AeroGauge) ⭐ 29 | 🐛 0 | 🌐 C | 📅 2026-01-23 - An in-progress decompilation of *AeroGauge*
* [F-Zero X Expansion Kit](https://github.com/inspectredc/fzerox-expansion-kit) ⭐ 27 | 🐛 0 | 🌐 C | 📅 2026-01-06 - An in-progress decompilation of the *F-Zero X Expansion Kit*
* [Gex 64: Enter the Gecko](https://github.com/matbourgon/gex64decomp) ⭐ 27 | 🐛 12 | 🌐 C | 📅 2026-07-27 - An in-progress decompilation of *Gex 64: Enter the Gecko*
* [Turok 3: Shadow of Oblivion](https://github.com/Drahsid/turok3) ⚠️ Archived - An in-progress decompilation of *Turok 3: Shadow of Oblivion*
* [Virtual Pro Wrestling 2: Ōdō Keishō](https://github.com/aki-club/vpw2) ⭐ 26 | 🐛 0 | 🌐 Assembly | 📅 2026-03-26 - An in-progress decompilation of *Virtual Pro Wrestling 2: Ōdō Keishō*
* [Gauntlet Legends](https://github.com/Drahsid/gauntlet-legends) ⭐ 25 | 🐛 0 | 🌐 C | 📅 2026-04-30 - An in-progress decompilation of *Gauntlet Legends*
* [Mario Golf](https://github.com/monde-lointain/mariogolf64) ⭐ 22 | 🐛 1 | 🌐 C | 📅 2026-07-24 - An in-progress decompilation of *Mario Golf*
* [Superman 64](https://github.com/farisawan-2000/superman) ⭐ 22 | 🐛 0 | 🌐 Assembly | 📅 2021-04-17 - An in-progress decompilation of *Superman 64*
* [Star Wars: Shadows of the Empire](https://github.com/eltalelibrarian/sote) ⭐ 18 | 🐛 1 | 🌐 C | 📅 2025-02-10 - An in-progress decompilation of *Star Wars: Shadows of the Empire*
* [Duke Nukem 64](https://github.com/nblood/duke64-re) ⭐ 17 | 🐛 0 | 🌐 C | 📅 2025-08-04 - An in-progress decompilation of *Duke Nukem 64*
* [Quest 64](https://github.com/Rainchus/quest64-decomp) ⭐ 17 | 🐛 1 | 🌐 C | 📅 2026-02-03 - An in-progress decompilation of *Quest 64*
* [Bomberman 64: The Second Attack!](https://github.com/bomberhackers/tsa) ⭐ 13 | 🐛 0 | 🌐 C | 📅 2026-04-04 - An in-progress decompilation of *Bomberman 64: The Second Attack!*
* [Glover](https://github.com/Rainchus/glover) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2025-03-13 - An in-progress decompilation of *Glover*
* [Mario Tennis](https://github.com/dellm-79/mariotennisn64) ⭐ 11 | 🐛 0 | 🌐 C | 📅 2024-04-05 - An in-progress decompilation of *Mario Tennis*
* [Chameleon Twist](https://github.com/chameleontwistret/chameleontwistv1.0-jp) ⭐ 10 | 🐛 0 | 🌐 C | 📅 2026-08-19 - An in-progress decompilation of *Chameleon Twist*
* [Mystical Ninja Starring Goemon](https://github.com/klorfmorf/mnsg) ⭐ 9 | 🐛 0 | 🌐 C | 📅 2026-06-28 - An in-progress decompilation of *Mystical Ninja Starring Goemon*
* [Knife Edge: Nose Gunner](https://github.com/disi33/KE-NG_Reversing) ⭐ 7 | 🐛 0 | 🌐 Shell | 📅 2021-04-01 - Configures a reverse engineering environment (Mupen64+ RE, Ghidra, etc.) for *Knife Edge: Nose Gunner*
* [Lego Racers](https://github.com/marijnvdwerf/lego-racers) ⭐ 7 | 🐛 1 | 🌐 Python | 📅 2025-09-14 - An in-progress decompilation of *Lego Racers*
* [Shadowgate 64](https://github.com/Rainchus/shadowgate64) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2023-05-18 - An in-progress decompilation of *Shadowgate 64*
* [Virtual Pool 64](https://github.com/LLONSIT/virtualpool64) ⭐ 7 | 🐛 0 | 🌐 Assembly | 📅 2022-10-29 - An in-progress decompilation of *Virtual Pool 64*
* [Doraemon: Nobita to Mittsu no Seireiseki](https://github.com/prakxo/doraemon1) ⭐ 6 | 🐛 0 | 🌐 C | 📅 2026-08-29 - An in-progress decompilation of *Doraemon: Nobita to Mittsu no Seireiseki*
* [The New Tetris](https://github.com/kiritodv/tnt) ⚠️ Archived - An in-progress decompilation of *The New Tetris*
* [Chameleon Twist 2](https://github.com/chameleontwistret/chameleontwist2v1.0-jp) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2026-05-18 - An in-progress decompilation of *Chameleon Twist 2*
* [Dark Rift](https://github.com/unnunu/darkrift) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2026-06-23 - An in-progress decompilation of *Dark Rift*
* [Onegai Monsters](https://github.com/ryan-myers/onegaimonsters) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2025-11-20 - An in-progress decompilation of *Onegai Monsters*
* [Sharkwire 64](https://github.com/Jhynjhiruu/sharkwire) ⭐ 2 | 🐛 0 | 🌐 Assembly | 📅 2025-05-08 - An in-progress decompilation of the SharkWire Online cartridge firmware
* [Banjo-Kazooie](https://gitlab.com/banjo.decomp/banjo-kazooie) - A **complete** decompilation of *Banjo-Kazooie*
* [Donkey Kong 64](https://gitlab.com/dk64_decomp/dk64) - An in-progress decompilation of *Donkey Kong 64*
* [GoldenEye 007](https://gitlab.com/kholdfuzion/goldeneye_src) - An in-progress decompilation of *GoldenEye 007*
* [Perfect Dark](https://gitlab.com/ryandwyer/perfect-dark) - A **complete** decompilation of *Perfect Dark* (see also [pdtools](https://gitlab.com/ryandwyer/pdtools))
* [Star Fox 64](https://github.com/sonicdcer/sf64) - An in-progress decompilation of *Star Fox 64*

#### Other

* [UltraCIC](https://github.com/mikeryan/UltraCIC) ⭐ 103 | 🐛 1 | 🌐 Assembly | 📅 2018-08-19 - A clone of the CIC copy protection chip
* [UltraPIF](https://github.com/jago85/UltraPIF_Hardware) ⭐ 79 | 🐛 5 | 📅 2020-10-30 - A replacement for the PIF chip that enables a region-free console
* [UltraCIC-III](https://github.com/ManCloud/UltraCIC-III) ⭐ 54 | 🐛 4 | 🌐 C++ | 📅 2022-12-08 - Code for a replacement CIC chip on an ATTiny25/45/85
* [f3dex2](https://github.com/Mr-Wiseguy/f3dex2) ⭐ 50 | 🐛 1 | 🌐 C | 📅 2026-05-24 - Matching and mostly documented disassemblies of the F3DEX2/F3DZEX2 N64 RSP microcode family
* [UltraCIC\_C](https://github.com/jago85/UltraCIC_C) ⭐ 37 | 🐛 0 | 🌐 C | 📅 2019-08-23 - Another CIC implementation (same name, but a separate implementation)
* [UltraCIC-II](https://github.com/perkinsb1024/UltraCIC-II) ⭐ 36 | 🐛 0 | 🌐 Assembly | 📅 2019-01-13 - Code to recreate CIC chips on an ATTiny25/45
* [nus-cpu](https://github.com/dmkfasi/nus-cpu) ⭐ 34 | 🐛 0 | 🌐 Prolog | 📅 2020-12-14 - A condensed, modular re-creation of the Nintendo 64 motherboard
* [n64-kicad](https://github.com/nterry/n64-kicad/) ⭐ 19 | 🐛 0 | 📅 2021-01-30 - A set of KiCad files detailing the Nintendo 64 hardware
* [N64 Uncompiled Source Code](http://shygoo.net/n64-uncompiled/) - Various source code and related material discovered in various ROM images
* [shogihax](https://cturt.github.io/shogihax.html) - Details a remote code execution exploit of the Nintendo 64 via the *Morita Shogi 64* cartridge and its dialup modem
* [Ultra FP64](http://www.ultrafp64.com/) - A work in progress FPGA Nintendo 64

### Guides and Reference

* [awesome-decompilation](https://github.com/nforest/awesome-decompilation/blob/master/README.md) ⭐ 667 | 🐛 4 | 📅 2023-11-09 - A curated list of awesome decompilation resources and projects
* [n64-decompiling](https://www.retroreversing.com/n64-decompiling) - An overview of decompiling Nintendo 64 ROMs with Ghidra

### Tools and Disassemblers

* [m2c](https://github.com/matt-kempster/m2c) ⭐ 632 | 🐛 65 | 🌐 Python | 📅 2026-08-30 - An open-source MIPS decompiler, useful for understanding and reimplementing N64 games' behavior in C
* [GEDecompressor](https://github.com/jombo23/N64-Tools/tree/master/GEDecompressor) ⭐ 333 | 🐛 39 | 🌐 C++ | 📅 2026-07-26 - Decompressor for a wide variety of compression formats used across various titles
* [decomp-permuter](https://github.com/simonlindholm/decomp-permuter) ⭐ 217 | 🐛 49 | 🌐 Python | 📅 2026-08-22 - A tool to randomly permute C files to better match a target binary
* [rabbitizer](https://github.com/decompollaborate/rabbitizer) ⭐ 179 | 🐛 2 | 🌐 C | 📅 2026-05-29 - An API for decoding MIPS instructions
* [asm-differ](https://github.com/simonlindholm/asm-differ) ⭐ 167 | 🐛 34 | 🌐 Python | 📅 2026-08-25 - A `diff` script for MIPS assembly
* [N64LoaderWV](https://github.com/zeroKilo/N64LoaderWV) ⭐ 166 | 🐛 1 | 🌐 Java | 📅 2026-08-01 - Nintendo 64 ROM loader for the [Ghidra](https://github.com/NationalSecurityAgency/ghidra) ⭐ 74,211 | 🐛 1,920 | 🌐 Java | 📅 2026-09-01 reverse engineering tool
* [spimdisasm](https://github.com/decompollaborate/spimdisasm) ⭐ 79 | 🐛 7 | 🌐 Python | 📅 2026-08-06 - Matching MIPS disassembler API and front-ends with built-in instruction analysis
* [n64sym](https://github.com/shygoo/n64sym) ⭐ 45 | 🐛 1 | 🌐 Standard ML | 📅 2023-03-27 - Scans a RAM dump for symbols from a given library or object file
* [bdiff](https://github.com/ethteck/bdiff) ⭐ 25 | 🐛 17 | 🌐 Rust | 📅 2024-11-04 - A local binary diffing tool
* [m3c](https://github.com/ethteck/m3c) ⭐ 13 | 🐛 3 | 🌐 Python | 📅 2024-05-01 - A tool to assist with N64 decompilation that runs [m2c](https://github.com/matt-kempster/m2c) ⭐ 632 | 🐛 65 | 🌐 Python | 📅 2026-08-30 and [decomp-permuter](https://github.com/simonlindholm/decomp-permuter) ⭐ 217 | 🐛 49 | 🌐 Python | 📅 2026-08-22 to try to automatically decompile functions
* [openocd\_n64](https://github.com/juchong/openocd_n64) ⭐ 1 | 🐛 0 | 📅 2021-03-09 - An [OpenOCD](http://openocd.org/doc/html/About.html) configuration for the Nintendo 64 CPU
* [Compiler Explorer](https://godbolt.org) - Explore how your C, C++, Rust, or other compiled language code ends up looking after compilation
* [Online Disassembler](https://onlinedisassembler.com/odaweb/) - A lightweight, online service for when you don't have the time, resources, or requirements to use a heavier-weight alternative
* [RI Probe](https://www.romhacking.net/homebrew/102/) - A ROM that dumps RDRAM values onscreen for debugging and exploring

## Programming

### Assembly

* [sodium64](https://github.com/Hydr8gon/sodium64) ⭐ 326 | 🐛 21 | 🌐 Assembly | 📅 2025-07-11 - A SNES emulator for the N64, written in assembly
* [PeterLemon/N64](https://github.com/PeterLemon/N64) ⭐ 323 | 🐛 17 | 🌐 Assembly | 📅 2026-02-01 - Nintendo 64 bare metal MIPS assembly programming reference
* [n64ops](https://github.com/mikeryan/n64dev/tree/master/docs/n64ops) ⭐ 174 | 🐛 1 | 🌐 C | 📅 2018-11-02 - R4300i, RCP, and RSP opcode details
* [neon64v2](https://github.com/hcs64/neon64v2) ⭐ 109 | 🐛 22 | 🌐 Assembly | 📅 2025-01-06 - An original Nintendo Entertainment System emulator, written in assembly
* [n64-assembly](https://github.com/is06/n64-assembly) ⭐ 13 | 🐛 0 | 📅 2020-10-30 - A [Visual Studio Code](https://code.visualstudio.com/) extension that provides language support and theme for the Nintendo 64 assembly language
* [N64-ASM-Tutorial](https://github.com/fraser125/N64-ASM-Tutorial) ⭐ 11 | 🐛 0 | 🌐 Assembly | 📅 2018-08-27 - The support files for N64 Assembly Language Tutorial
* [n64-asm-timing](https://github.com/pdrome/n64-asm-timing) ⭐ 5 | 🐛 0 | 🌐 Assembly | 📅 2018-04-25 - Nintendo 64 CPU instruction timing
* [Fraser N64](https://www.youtube.com/channel/UC3tcfSES8CB45DmTbHhUP1w) - YouTube channel featuring Nintendo 64 assembly programming
* [N64 Assembly Language Tutorial](https://sites.google.com/site/consoleprotocols/home/homebrew/n64-assembly-home) - Fraser's detailed Nintendo 64 assembly programming guide
* [N64 ASM Tutorials](https://patater.com/gbaguy/n64asm.htm) - Nintendo 64 assembly language programming tutorials by Mike Huber (mirrored by Jaeden Amero)
* [cubeworld](https://gitlab.com/is06/cubeworld) - The beginnings of an experimental game, written in assembly

### C

#### Guides

* [N64 Homebrew Starter Guide](https://drive.google.com/drive/folders/1rOE2zYV2RPPx-2NHRGiGZ-RFx6w_6dAI) - Buu342's guide to creating an N64 game with the official SDK
* [Implementation of Sounds Using the Nintendo 64 Sound Tools](https://docs.google.com/document/d/1d1qKxMh3q_89w9N76xL9bXRqkXe1ylcDnAtg3cgu5s8) - Buu342's guide to implementing sound in your ROM with the Nintendo 64 Sound Tools
* [N64Squid Homebrew](https://n64squid.com/homebrew/n64-sdk) - Development walkthrough using the NuSystem library that's part of the official SDK
* [moria.us #nintendo-64](https://www.moria.us/tags/nintendo-64) - A series of blog posts covering a broad range of Nintendo 64 development topics

#### Example Code

* [pyrite64](https://github.com/HailToDodongo/pyrite64) ⭐ 3,244 | 🐛 23 | 🌐 C++ | 📅 2026-08-20 - A game engine and editor using `libdragon` and `tiny3d` from C++

* [ClassiCube](https://github.com/ClassiCube/ClassiCube) ⭐ 2,043 | 🐛 564 | 🌐 C | 📅 2026-08-27 - A multi-platform Minecraft Classic / ClassiCube client with early N64 support, using `libdragon`

* [N64-RPG](https://github.com/breadbored/N64-RPG) ⭐ 185 | 🐛 2 | 🌐 C | 📅 2023-12-06 - An in-progress RPG engine using `libdragon`

* [UltraEd](https://github.com/deadcast2/UltraEd/) ⚠️ Archived - An in-progress level editor and game engine

* [Legend of Elya](https://github.com/Scottcjn/legend-of-elya-n64) ⭐ 130 | 🐛 3 | 🌐 C | 📅 2026-08-30 - A 4-layer nano-GPT neural network (819K parameters) running natively on the N64's MIPS R4300i FPU, believed to be the first LLM on Nintendo 64 hardware

* [gb64](https://github.com/lambertjamesd/gb64) ⭐ 107 | 🐛 21 | 🌐 C | 📅 2024-08-17 - A Nintendo Game Boy emulator that runs on real hardware

* [64doom](https://github.com/jnmartin84/64doom) ⭐ 98 | 🐛 12 | 🌐 C++ | 📅 2024-03-17 - A source port of the original *DOOM*

* [goose64](https://github.com/jsdf/goose64) ⭐ 86 | 🐛 1 | 🌐 C++ | 📅 2023-12-03 - jsdf's *Untitled Goose Game* "demake"

* [n64-sdk-demo](https://github.com/jsdf/n64-sdk-demo) ⭐ 73 | 🐛 2 | 🌐 Objective-C | 📅 2020-06-14 - jsdf's detailed example with heavily-commented source showing basic usage of the official SDK and the NuSystem library

* [N64brew Game Jam 2024](https://github.com/n64brew/N64brew-GameJam2024) ⭐ 71 | 🐛 0 | 🌐 C | 📅 2025-12-29 - A collaborative minigame ROM for the N64brew Game Jam 2024

* [n64\_controller\_test](https://github.com/Ryzee119/n64_controller_test) ⭐ 70 | 🐛 0 | 🌐 C | 📅 2024-11-06 - A simple homebrew ROM built with `libdragon` to perform some basic controller tests

* [FlappyBird-N64](https://github.com/meeq/FlappyBird-N64) ⭐ 56 | 🐛 0 | 🌐 C | 📅 2026-01-05 - A demake of *Flappy Bird* using `libdragon`

* [Mine64](https://github.com/SiliconSloth/Mine64) ⭐ 46 | 🐛 0 | 🌐 C | 📅 2025-02-02 - A Minecraft clone, using Nintendo's NuSystem library

* [mvs64](https://github.com/rasky/mvs64) ⭐ 39 | 🐛 3 | 🌐 C | 📅 2024-08-17 - A NeoGeo emulator

* [ultra64demos](https://github.com/shlomnissan/ultra64demos) ⭐ 38 | 🐛 0 | 🌐 C | 📅 2014-02-20 - Original SGI Nintendo 64 technical demos

* [small64](https://github.com/rasky/small64) ⭐ 36 | 🐛 0 | 🌐 C++ | 📅 2025-07-13 - The first Nintendo 64 4K intro (a demoscene executable that produces visuals and music using 4KB or less)

* [N64-NetLib](https://github.com/buu342/N64-NetLib) ⭐ 35 | 🐛 2 | 🌐 C++ | 📅 2025-08-20 - A set of tools and libraries to connect your Nintendo 64 homebrew to the internet

* [Driving Strikers 64](https://github.com/SpookyIluha/Driving-Strikers-64) ⭐ 29 | 🐛 0 | 🌐 C | 📅 2025-07-22 - A Nintendo 64 port of the indie Dreamcast game *Driving Strikers* using `libdragon` and `tiny3d`

* [Controller-Pak-Manager](https://github.com/manfriedn64/Controller-Pak-Manager) ⭐ 26 | 🐛 0 | 🌐 C | 📅 2020-05-06 - A ROM that presents graphical user interface to manage Controller Pak data

* [controllertest](https://github.com/max257612/controllertest) ⭐ 20 | 🐛 0 | 🌐 C | 📅 2020-10-09 - Another controller test ROM, also built with `libdragon`

* [rsp-ruination](https://github.com/Dillonb/rsp-ruination) ⭐ 17 | 🐛 0 | 🌐 C | 📅 2024-08-31 - A torture test that uses an emulated RSP on the CPU to validate functionality of the actual RSP

* [n64-gba](https://github.com/Dillonb/n64-gba) ⭐ 16 | 🐛 0 | 🌐 C | 📅 2022-10-04 - A proof of concept Game Boy Advance emulator (only runs ARMWrestler, a CPU exercise ROM)

* [n64triangle](https://github.com/sp1187/n64triangle) ⭐ 15 | 🐛 0 | 🌐 C | 📅 2025-07-22 - RDP triangle demo, using `libdragon`

* [BrewReality](https://github.com/SpookyIluha/BrewReality) ⭐ 12 | 🐛 0 | 🌐 C | 📅 2025-01-14 - A 3D flight simulator tech demo built with `libdragon`, featuring 128x128 textures and dynamic sky and lighting

* [cmake-demo-rom](https://github.com/N64-tools/cmake-demo-rom) ⚠️ Archived - Demonstrates building toolchains and a ROM using CMake and `libdragon`

* [brick64](https://github.com/allie/brick64) ⭐ 9 | 🐛 0 | 🌐 C | 📅 2020-08-23 - A homebrew 3D brick-breaker game using the official SDK

* [shibamatch](https://github.com/einhov/shibamatch) ⭐ 9 | 🐛 1 | 🌐 C | 📅 2019-08-08 - A Shiba Inu-themed memory match game

* [ultra64-templates](https://github.com/stefanmielke/ultra64-templates) ⭐ 9 | 🐛 11 | 🌐 C | 📅 2025-02-05 - Game templates/starting points for use with n64sdkmod

* [aw64](https://github.com/jnmartin84/aw64) ⭐ 8 | 🐛 0 | 🌐 C++ | 📅 2022-08-23 - (C++) A Nintendo 64 port of the bytecode interpreter from *Another World*/*Out of This World*

* [non\_nusys\_demo](https://github.com/gamemasterplc/non_nusys_demo) ⭐ 8 | 🐛 0 | 🌐 C | 📅 2021-05-23 - A complex demo built without relying on Nintendo's NuSystem library

* [ochim](https://github.com/murachue/ochim) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2020-04-04 - An up to 4 player action puzzle game

* [Memory64-N64](https://github.com/vieux/Memory64-N64) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2025-11-10 - A Simon style memory game with Rumble Pak support, using libdragon

* [n64\_bullet\_demo](https://github.com/alexvnesta/n64_bullet_demo) ⭐ 7 | 🐛 1 | 🌐 Makefile | 📅 2023-12-27 - An example of using Bullet Physics with `libdragon`'s OpenGL branch to create physics simulations

* [old-castle](https://github.com/danbolt/old-castle) ⭐ 6 | 🐛 2 | 🌐 C | 📅 2023-03-05 - A homebrew game based on a NuSystem sample from the official SDK

* [helloworld](https://github.com/loociano/n64dev/tree/master/helloworld) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2018-06-11 - Hello World example using NuSystem and S2DEX microcode

* [n64-gameoflife](https://github.com/jsdf/n64-gameoflife) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2020-04-20 jsdf's implementation of the classic *Conway's Game of Life*

* [platformer64](https://github.com/lambertjamesd/platformer64) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2020-10-07 - An in-progress adventure platformer

* [vlak64](https://github.com/thekovic/vlak64) ⭐ 5 | 🐛 0 | 🌐 C | 📅 2026-02-06 - A reimplementation of the classic DOS game *Vlak* using `libdragon`

* [n64zlibbench](https://github.com/clbr/n64zlibbench) ⭐ 4 | 🐛 0 | 🌐 C | 📅 2018-12-07 - A zlib benchmark with result display

* [BrewChristmas](https://github.com/SpookyIluha/BrewChristmas) ⭐ 3 | 🐛 0 | 🌐 C | 📅 2025-01-25 - A single 3D holiday scene built using `libdragon` and `tiny3d`

* [chip8-n64](https://github.com/joshiggins/chip8-n64) ⭐ 3 | 🐛 1 | 🌐 C | 📅 2024-08-17 - A [CHIP-8](https://en.wikipedia.org/wiki/CHIP-8) emulator, using `libdragon`

* [paniclab64](https://github.com/1r3n33/paniclab64) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2021-05-09 - A homebrew game inspired by *Panic Lab* from Gigamic

* [SpaceCube64](https://github.com/realtradam/tojam2024) ⭐ 2 | 🐛 0 | 🌐 C | 📅 2024-05-17 - A space-like shooter game made in a weekend for TOJam 2024

* [Pong64](https://github.com/JumpiX64/Pong64) ⭐ 1 | 🐛 0 | 🌐 C | 📅 2026-06-28 - A port of Pong featuring additional game modes, using `libdragon`

* [Happy Little Frog Game](https://github.com/s4Ys369/hlfg) ⭐ 1 | 🐛 0 | 🌐 C | 📅 2025-09-01 - An in-progress platformer made with `libdragon` and `tiny3d`

* [CounterEmotion-Bar](https://github.com/SpookyIluha/CounterEmotion-Bar) ⭐ 1 | 🐛 0 | 🌐 C | 📅 2025-08-06 - A Targem Games 3-Day GameJam 2025 entry built with `libdragon` and `tiny3d`

* [hash-bench-n64](https://github.com/dmang-dev/hash-bench-n64) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2026-05-14 - Hash-algorithm benchmark ROM that times 32 cryptographic and non-cryptographic hashes (CRC, MD5, SHA-1, SHA-512, BLAKE2s, etc.) on the VR4300 and displays µs/iter and KB/s on screen, using `libdragon`

* [N64brew Game Jam 2020](https://github.com/N64brew-Game-Jam-2020) - N64brew Game Jam 2020 submissions

* [N64brew Game Jam 2021](https://github.com/N64brew-Game-Jam-2021) - N64brew Game Jam 2021 submissions

* [N64brew Game Jam 2022](https://github.com/N64brew-Game-Jam-2022) - N64brew Game Jam 2022 submissions

* [N64brew Game Jam 2023](https://github.com/N64brew-Game-Jam-2023) - N64brew Game Jam 2023 submissions

* [N64brew Game Jam 2025](https://github.com/N64brew-Game-Jam-2025) - N64brew Game Jam 2025 submissions

* [Penguins Luv Melons](https://n64squid.com/penguins-luv-melons/) - A homebrew game built with `libdragon`

### Rust

* [cargo-n64](https://github.com/rust-console/cargo-n64) ⭐ 169 | 🐛 13 | 🌐 Rust | 📅 2022-06-21 - A `cargo` subcommand to build Nintendo 64 ROMs in Rust
* [n64-systemtest](https://github.com/lemmy-64/n64-systemtest) ⭐ 94 | 🐛 13 | 🌐 Rust | 📅 2026-07-21 - A collection of hardware tests written in Rust
* [rrt0/examples](https://github.com/rust-console/rrt0/tree/main/examples) ⭐ 19 | 🐛 1 | 🌐 Rust | 📅 2024-10-16 - Rust examples using cargo-n64
* [rrt0](https://github.com/rust-console/rrt0) ⭐ 19 | 🐛 1 | 🌐 Rust | 📅 2024-10-16 - A simple cross-platform runtime / startup for Rust on embedded devices
* [libdragon-rs](https://github.com/sarchar/libdragon-rs) ⭐ 18 | 🐛 1 | 🌐 Rust | 📅 2025-01-16 - Rust bindings to `libdragon`
* [loka-n64](https://github.com/JoNil/loka-n64) ⭐ 17 | 🐛 1 | 🌐 Rust | 📅 2024-12-15 - Nintendo 64 tools (including `extract_boot_code`, useful for cargo-n64) and a work in progress game
* [nust64](https://github.com/bigbass1997/nust64) ⭐ 16 | 🐛 0 | 🌐 Rust | 📅 2024-06-26 - Rust crate for compiling a Rust project into an N64 ROM
* [n64-slides-apr](https://github.com/monocasa/n64-slides-apr) ⭐ 12 | 🐛 0 | 🌐 Rust | 📅 2020-05-19 - Source code for April 2019 Rust Meetup slides as a Nintendo 64 ROM
* [n64toolchain](https://github.com/monocasa/n64toolchain) ⭐ 9 | 🐛 0 | 🌐 Rust | 📅 2016-12-26 - Rust Implementation of a Nintendo 64 ROM toolchain
* [n64rom-rs](https://github.com/saneki/n64rom-rs) ⭐ 9 | 🐛 0 | 🌐 Rust | 📅 2021-01-10 - A library and toolkit for working with ROMs
* [rs64-rt](https://github.com/monocasa/rs64-rt) ⭐ 5 | 🐛 0 | 🌐 Rust | 📅 2019-04-18 - Minimal Rust startup / runtime for Nintendo 64
* [rs64-periph](https://github.com/monocasa/rs64-periph) ⭐ 5 | 🐛 1 | 🌐 Rust | 📅 2021-02-07 - Fairly raw N64 MMIO definitions
* [rs64-rom](https://github.com/monocasa/rs64-rom) ⭐ 5 | 🐛 0 | 🌐 Rust | 📅 2019-04-17 - Rust library for manipulating ROMs
* [libdragon-bindings](https://github.com/DagothBob/libdragon-bindings) ⭐ 5 | 🐛 1 | 🌐 Rust | 📅 2021-05-11 - Rust bindings and interface for `libdragon`
* [rs64romtool](https://github.com/monocasa/rs64romtool) ⭐ 5 | 🐛 0 | 🌐 Rust | 📅 2019-04-18 - Tool for manipulating ROMs (depends on rs64-rom)

### Go

* [clktmr/n64](https://github.com/clktmr/n64) ⭐ 46 | 🐛 0 | 🌐 Go | 📅 2026-07-09 - Support for Nintendo 64 in [embeddedgo](https://embeddedgo.github.io)
* [gopher-kart](https://github.com/clktmr/gopher-kart) ⭐ 11 | 🐛 0 | 🌐 Go | 📅 2025-08-03 - A port of the original gopher-kart browser game to demo Go support
* [Getting Started with Go](https://www.timurcelik.de/posts/n64go-1-getting-started/) - A blog post about building a ROM in Go, covering framebuffer output, controller polling, and audio playback

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-09-01._
