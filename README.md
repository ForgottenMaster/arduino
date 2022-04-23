# Arduino
This is a repository for me to do work fiddling with my Arduino Uno in Rust as I experiment with embedded coding.

To run the binaries in this package is just a case of using cargo run and ensuring the Arduino Uno is plugged into the computer so the compiled program can be uploaded.

However there are a few external dependencies required to be installed on the computer that cargo run won't install for you

**AVR tools**
The first dependency is the tools/compiler required to produce the executables, the method of installing will be different depending on operating system.

On Ubuntu, the following command can be used:
```
sudo apt install avr-libc gcc-avr pkg-config avrdude
```

On Windows, the base tools can be installed with WinAVR: https://sourceforge.net/projects/winavr/files/

However, this is fairly old, and the version of avrdude that comes with it is old. This package will require a version of at least **6.3** so grab the latest version of avrdude from here: https://github.com/mariusgreuel/avrdude/releases

Copy the updated avrdude executable over the version that WinAVR installed.

**ravedude**
This is a tool that handles flashing the Arduino device for you, and integrates seamlessly with cargo run, installation of this is cross-platform as it can be installed through cargo with the following:
```
cargo install ravedude
```
