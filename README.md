This is a temporal (I hope!) fork of the Atari800 emulator port for Raspberry Pi.
I included two configuration file entries for PAL and NTSC physical monitor refresh rates.
These options are:
MONITOR_REFRESH_RATE_PAL=<double>
MONITOR_REFRESH_RATE_NTSC=<double>

These new options allow to run the emulator with the same exact framerate that your physical screen uses
at the configured resolution, thus allowing perfect smooth scrolls in games and demos, just like in 
the original hardware.
The right values can be obtained from RetroArch, for example.
If you don't use the right values, you may get occasional frame desyncs ("jumps" in smooth scroll games/demos).

I also changed the build system so it doesn't require a crosscompilation enviroment anymore and will build
natively on the Pi. This is because I tend to use distributed compilation enviroments instead of cross compilation.

To build, just cd into the src directory and run "make". A Raspberry-Pi Makefile is ready to use.
