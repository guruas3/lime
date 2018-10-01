Building from Source
====================

Clone the Lime repository, as well as the submodules:

    git clone -b native --recursive https://github.com/guruas3/lime.git native

Tell haxelib where your development copy of Lime is installed:

    haxelib dev lime native

The first time you run the "lime" command, it will attempt to build the Lime standard binary for your desktop platform as the command-line tools. To build these manually, use the following command (using "mac" or "linux" if appropriate):

    haxelib install format
    lime rebuild windows

You can build additional binaries, or rebuild binaries after making changes, using "lime rebuild":

    lime rebuild windows
    lime rebuild linux -64 -release -clean

You can also rebuild the tools if you make changes to them:

    lime rebuild tools

On a Windows machine, you should have Microsoft Visual Studio C++ (Express is just fine) installed. You will need Xcode on a Mac. To build on a Linux machine, you may need the following packages (or similar):

    sudo apt-get install libgl1-mesa-dev libglu1-mesa-dev g++ g++-multilib gcc-multilib libasound2-dev libx11-dev libxext-dev libxi-dev libxrandr-dev libxinerama-dev

To switch away from a source build, use:

    haxelib dev lime

Targets
=======

Lime currently supports the following targets:

    lime test windows
    lime test mac
    lime test linux
    lime test neko
    lime test android
    lime test ios
    lime test html5
    lime test flash
    lime test air

Desktop builds are currently designed to be built on the same host OS
