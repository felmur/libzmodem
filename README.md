# libzmodem
Zmodem protocol under TCP/IP

# HOWTO Compile & Install
Open a shell in the source directory and then type:
```
mkdir build
cd build
cmake ../
make
sudo make install
```
# Files
libzmodem.so, the library itself, goes under /usr/lib

zmodem.h, the include for library, goes under /usr/include

msz, a zmodem sender, executable, goes under /usr/bin

mrz, a zmodem receiver, executable, goes under /usr/bin

# WARNING
This library does not appear to work properly with other programs that implement the zmodem protocol. In particular, when running msz and receiving files with a program other than mrz, numerous bad CRC errors are reported.

# Credits
This library is not my own work. 
I have tried unsuccessfully to compile this library under Archlinux:

[https://github.com/spk121/libzmodem](https://github.com/spk121/libzmodem)

So, I decided to fix it so that it could easily be compiled with cmake.

Thanks to Uwe Ohse, Chuck Forsberg, and Michael L. Gran for creating these routines.

