How to install Gromacs
=======================


* descargar gromacs
* Descomprimir usando tar xvf paquete
* Descargar regressiontest
* Descomprimir el regresssiontest y ponerlo sobre la path de gromacs
* Ejecutar sobre el directorio descomprimido de gromacs:
    mkdir build
    cd build
    cmake .. -DCMAKE_INSTALL_PREFIX=/opt/gromacs/2020.5 -DGMX_MPI=on -DGMX_GPU=on -DCMAKE_C_COMPILER=mpicc -DCMAKE_CXX_COMPILER=mpicxx -DGMX_BUILD_OWN_FFTW=ON -DREGRESSIONTEST_PATH=/opt/gromacs/

Esto usa la GPU.

Mirar INSTALL para obtener el link del regressiontest.

* make -j <n> en donde n es el número de procesadores a utilizar
* make install


Para actualizar el Colvars se debe descargar el paquete:

https://github.com/Colvars/colvars/blob/master/README.md#gromacs-colvars-releases

* Se descomprime
* cd DIR
* mkdir build && cd build
* cmake .. -DCMAKE_INSTALL_PREFIX=/opt/gromacs/2020.5 -DGMX_MPI=on -DGMX_GPU=on -DCMAKE_C_COMPILER=mpicc -DCMAKE_CXX_COMPILER=mpicxx -DGMX_BUILD_OWN_FFTW=ON -DREGRESSIONTEST_PATH=/opt/gromacs/

es la misma instrucción de la instalación.

* make -j <n>
* make install

Revisar con history posible instalaciones manuales de gcc y cmake
