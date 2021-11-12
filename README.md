# Thorium-Special
Special builds of Thorium

Simply a seperate repo for builds of Thorium https://github.com/Alex313031/Thorium that have modified compiler flags flags or args.gn flags for specific processors or use cases.

You can modify BUILD.gn (which goes in //chromium/build/config/compiler/) to suit your system by referring to the list of microarchitectures and associated -march flags here > https://gcc.gnu.org/onlinedocs/gcc/x86-Options.html

You could modify args.gn by referencing > https://github.com/Alex313031/Thorium/blob/main/args.list
