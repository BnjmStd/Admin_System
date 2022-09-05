How to compile GCC
===================================


Instalar GCC 9.4

Instalación de dependencias:

[GMP]
GMP is the GNU Multiple Precision Arithmetic Library, GMP utiliza sus propias optimizaciones con detección de CPU incluida.
wget https://gmplib.org/download/gmp/gmp-6.2.1.tar.xz
tar Jxvf gmp-6.2.1.tar.xz
cd gmp-6.2.1
./configure --disable-shared --enable-static --prefix=/tmp/gcc
make -j32 && make check -j32
su -c 'make install'

[MPFR]
MPFR is the GNU Multiple-precision floating-point rounding library. It depends on GMP.
wget http://www.mpfr.org/mpfr-current/mpfr-4.1.0.tar.xz
tar Jxvf mpfr-4.1.0.tar.xz
cd mpfr-4.1.0
./configure --disable-shared --enable-static --prefix=/tmp/gcc --with-gmp=/tmp/gcc
make -j32 && make check -j32
su -c 'make install'


[MPC]
MPC is the GNU Multiple-precision C library. It depends on GMP and MPFR.
wget ftp://ftp.gnu.org/gnu/mpc/mpc-1.2.1.tar.gz
tar zxvf mpc-1.2.1.tar.gz
cd mpc-1.2.1
make -j32 && make check -j32
su -c 'make install'

[ISL]
wget ftp://gcc.gnu.org/pub/gcc/infrastructure/isl-0.18.tar.bz2
bunzip2 isl-0.18.tar.bz2
tar xvf isl-0.18.tar
cd isl-0.18
./configure --with-gmp-prefix=/tmp/gcc --disable-shared --enable-static --prefix=/tmp/gcc
make -j32 && make check -j32
su -c 'make install'


[GCC]
wget https://ftp.gwdg.de/pub/misc/gcc/releases/gcc-11.2.0/gcc-11.2.0.tar.xz
tar Jxvf gcc-11.2.0.tar.xz
cd gcc-11.2.0
mkdir build && cd build
../configure --enable-shared --enable-threads=posix --enable-__cxa_atexit --enable-clocale=gnu --enable-languages=fortran,objc --program-suffix=11 --with-gmp=/tmp/gcc --with-mpfr=/tmp/gcc --with-mpc=/tmp/gcc --with-isl=/tmp/gcc --prefix=/share/apps/gcc/11.2/ --disable-multilib
make -j 16
su -c 'make install'
