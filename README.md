# Thorium-Special
Special builds of Thorium

Simply a seperate repo for builds of Thorium https://github.com/Alex313031/Thorium that have modified compiler flags flags or args.gn flags for specific processors or use cases.

## Building

Clone and do everything in https://github.com/Alex313031/Thorium except before building, copy the BUILD.gn file to //chromium/build/config/compiler/, and modify as per below.

You can modify BUILD.gn (which goes in //chromium/build/config/compiler/) to suit your system by referring to the list of microarchitectures and associated -march flags here > https://gcc.gnu.org/onlinedocs/gcc/x86-Options.html

You could modify args.gn by referencing the args.list file (also in Thorium repo).
