# olupu
macos only at the moment

## build local copy of Pd
```
# install compiler and git
git clone https://github.com/pure-data/pure-data.git
pure-data/
./autogen.sh 
./configure --enable-universal
# edit src/x_file.c :
# before the function file_do_copy, add the prototype:
# int snprintf(char *restrict s, size_t n, const char *restrict format, ...);
# (for some reasons, #include <stdio.h> isn't getting this proto
make
```

## use public kitcreator tool to build tclkit
http://kitcreator.rkeene.org/kits/building/a56ce7a079da9ae4a9a70ffac55d9f29afc1f39d/
and with the following options
* kitcreator version 0.12.1
* tcl version 8.6.11
* platform Mac OS X/amd64
* packages Tcllib TclX Tk TLS TclUDP
* kit threaded
* kit storage automatically determined
