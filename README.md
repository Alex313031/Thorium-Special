# Thorium-Special
Special builds of Thorium

Simply a seperate repo for builds of Thorium https://github.com/Alex313031/Thorium that have modified compiler flags flags or args.gn flags for specific processors or use cases. I will sometimes put builds that don't need AVX here.

Windows builds are here > https://github.com/Alex313031/Thorium-Win

Releases will have the architecture name in the name and the .deb package to differentiate them.

&ndash; NEW: Thorium Special now has experimental Android builds for ARM64. The tags will have ARM64 in the name.

I will be building for Vishera and Haswell CPUs (i.e. 2nd-Gen AMD FX "Vishera" and 4th-Gen Intel Core i Desktop/Mobile processors).

TODO: Make a component build for testing, and start building for haswell.

## Building

Clone and do everything in https://github.com/Alex313031/Thorium except before building, copy the contents of one of the build.gn files in this repo to //chromium/build/config/compiler/, and modify as per below.

You can modify BUILD.gn (which goes in //chromium/build/config/compiler/) to suit your system by referring to the list of microarchitectures and associated -march flags here > https://gcc.gnu.org/onlinedocs/gcc/x86-Options.html
You can use the contents of ICELAKE.gn, BULLDOZER.gn, HASWELL.gn, MSSE4.2.gn, MSSE4.0.gn, or MSSE3.gn. Theoretically, any CPU supporting at least SSE3 can have their -march dialed in to specifically target them for best performance.

You could modify args.gn by referencing the args.list file (also in the regular Thorium repo).
