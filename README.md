# libzmodem
Zmodem protocol under TCP/IP

# HOWTO Compile & Install
Open a shell in the source directory and then type:

mkdir build
cd build
cmake ../
make
sudo make install

# Files
libzmodem.so    library itself, goes under /usr/lib

zmodem.h        include for library, goes under /usr/include

msz             a zmodem sender, executable, goes under /usr/bin

mrz             a zmodem receiver, executable, goes under /usr/bin


# Credits
This library is not my own work. After repeatedly trying to compile this library:

[click here](https://github.com/spk121/libzmodem)

I decided to fix it so that it could easily be compiled with cmake.
