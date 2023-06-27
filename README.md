# RemoteIR Test Program
This project is a conversion of [RemoteIR_TestProgram](https://os.mbed.com/users/shintamainjp/code/RemoteIR_TestProgram/) by Shinichiro Nakamura to Mbed CE.  For more info, see the [cookbook page](https://os.mbed.com/cookbook/IR) and the [notebook page](https://os.mbed.com/users/shintamainjp/notebook/remote_ir_en/).

Note: As currently written, the code is designed to work with a Mbed LPC1768 board and an HD44780 LCD, plus appropriate infrared transmitted and/or receiver hardware.  If this is not your setup,
you may have to edit main.cpp, especially the pin assignments at the top, in order to compile the project.

## How to set up this project:

1. Clone it to your machine.  Don't forget to use `--recursive` to clone the submodules: `git clone --recursive https://github.com/mbed-ce/mbed-ce-hello-world.git`
2. Set up the GNU ARM toolchain (and other programs) on your machine using [the toolchain setup guide](https://github.com/mbed-ce/mbed-os/wiki/Toolchain-Setup-Guide).
3. Set up the CMake project for editing.  We have three ways to do this:
    - On the [command line](https://github.com/mbed-ce/mbed-os/wiki/Project-Setup:-Command-Line)
    - Using the [CLion IDE](https://github.com/mbed-ce/mbed-os/wiki/Project-Setup:-CLion)
    - Using the [VS Code IDE](https://github.com/mbed-ce/mbed-os/wiki/Project-Setup:-VS-Code)
4. Build the `flash-RemoteIR-Test-Program` target to upload the code to a connected device.