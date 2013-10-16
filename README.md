LZ4 Fast LZ Compressor
----------------------

LZ4 is a very fast lossless compression algorithm, providing compression
speed proportional to the memory bandwidth than the core speed, scalable
with multi-cores CPU.
It also features an extremely fast decoder, with speed in multiple GB/s
per core, typically reaching RAM speed limits on multi-core systems.

## Building

There are three flavour of build systems

### Autotools

If you are building from git you need a recent version of `autotools` and
you have to issue.

~~~
autoreconf -i
./configure
make
~~~

Packaged releases need a posix shell and make.

~~~
./configure
make
~~~

Out of tree build works

~~~
mkdir build
cd build
../configure
make
~~~

### CMake

Enter the cmake directory and run the usual

~~~
mkdir build
cd build
cmake ..
make
~~~

### Make

To use the plain makefile

~~~
make -f make/Makefile
~~~

## Contacts

The official [website](http://code.google.com/p/lz4/) contains most up to date
information and a bugtracker, a [forum](http://groups.google.com/group/lz4c) is also available.
