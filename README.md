# Thorium-Special
Special builds of Thorium

Simply a seperate repo for builds of Thorium https://github.com/Alex313031/Thorium that have modified compiler flags flags or args.gn flags for specific processors or use cases.

Right now BUILD.gn is set to icelake, but I will be building for Vishera and IceLake/Comet Lake CPUs (i.e. 2nd-Gen AMD FX "Vishera" and 10th-Gen Intel Core i Desktop/Mobile processors).

## Building

Clone and do everything in https://github.com/Alex313031/Thorium except before building, copy the BUILD.gn file in this repo to //chromium/build/config/compiler/, and modify as per below. (You can just copy the 'build' dir in this repo into //chromium/src)

You can modify BUILD.gn (which goes in //chromium/build/config/compiler/) to suit your system by referring to the list of microarchitectures and associated -march flags here > https://gcc.gnu.org/onlinedocs/gcc/x86-Options.html
It is set right now to "-march=icelake-client" but one could just search for "icelake" in a text editor and replace icelake-client with another -march from the link above.

You could modify args.gn by referencing the args.list file (also in the regular Thorium repo).
