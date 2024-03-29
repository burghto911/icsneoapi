icsneoapi
=========

A BSD-licensed open source library for communicating with vehicle network tools developed by Intrepid Control Systems. This library supports only a subset of devices and functionality.

Requires libftdi1.

```
$ sudo apt-get install libftdi1 libftdi-dev
```

On some distros (for example Ubuntu 14.04) libftdi1 doesn't create a symlink correctly for 64-bit versions. 
You'll need to point libftdi.so -> libftdi.so.1.

```
$ cd /usr/lib/x86_64-linux-gnu
$ sudo ln -s libftdi.so.1 libftdi.so
```

To build the library, simply make it.

```
$ make
```

You may wish to install the library and headers into your global folders so that other projects can utilize them. For example, on Ubuntu

```
$ sudo cp libicsneoapi.so /usr/lib/x86_64-linux-gnu/
$ sudo mkdir /usr/include/ics
$ sudo cp src/icsnVC40.h /usr/include/ics/
$ sudo cp src/icsneo40API.h /usr/include/ics/
```
