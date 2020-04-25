armv7-eabihf--musl--bleeding-edge-2020.02-2


Toolchains are hosted here: http://toolchains.bootlin.com/

All the licenses can be found here: http://toolchains.bootlin.com/downloads/releases/licenses/
All the sources can be found here: http://toolchains.bootlin.com/downloads/releases/sources/

PACKAGE      VERSION                 LICENSE
buildroot    2020.02-00011-g7ea8a52  GPL-2.0+
gcc-final    9.3.0                   unknown
binutils     2.33.1                  GPL-3.0+, libiberty LGPL-2.1+
gmp          6.1.2                   LGPL-3.0+ or GPL-2.0+
m4           1.4.18                  GPL-3.0+
mpc          1.1.0                   LGPL-3.0+
mpfr         4.0.2                   LGPL-3.0+
gcc-initial  9.3.0                   unknown
gdb          8.3                     GPL-2.0+, LGPL-2.0+, GPL-3.0+, LGPL-3.0+
expat        2.2.9                   MIT
pkgconf      1.6.1                   pkgconf license
ncurses      6.1                     MIT with advertising clause
patchelf     0.9                     GPL-3.0+
musl           1.1.24    MIT
linux-headers  4.19.107  GPL-2.0
gdb            8.3       GPL-2.0+, LGPL-2.0+, GPL-3.0+, LGPL-3.0+

For those who would like to reproduce the toolchain, you can just follow these steps:

    git clone https://github.com/bootlin/buildroot-toolchains.git buildroot
    cd buildroot
    git checkout toolchains.bootlin.com-2020.02-2

    curl http://toolchains.bootlin.com/downloads/releases/toolchains/armv7-eabihf/build_fragments/armv7-eabihf--musl--bleeding-edge-2020.02-2.defconfig > .config
    make olddefconfig
    make

This toolchain has been built, and the test system built with it has
successfully booted.
This doesn't mean that this toolchain will work in every cases, but it is at
least capable of building a Linux kernel with a basic rootfs that boots.
FLAG: TEST-OK
