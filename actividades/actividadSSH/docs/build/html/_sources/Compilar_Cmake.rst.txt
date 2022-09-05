How to compile CMAKE
===================================


Instalar cmake 3.21.3

[CMAKE]
wget https://github.com/Kitware/CMake/releases/download/v3.21.3/cmake-3.21.3.tar.gz
tar xvf cmake-3.21.3.tar.gz
cd cmake-3.21.3/
./bootstrap --prefix=/share/apps/cmake/3.21.3/ --parallel=16
make -j 16
su -c "make install"



** NOTA **
Revisar LD_LIBRAY_PATH.
Puede que existe una incompatibilidad.

Se deben cargar las librerías y módulos con el GCC-compilado

$ export LD_LIBRARY_PATH=/share/apps/gcc/11.2/lib64:/share/apps/gcc/11.2/lib
