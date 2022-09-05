How To Configure a Virtual Machine
===================================

Create a virtual machine
---------------------------------

La utilidad virt-manager permite a los usuarios crear máquinas virtuales usando una GUI. Para comenzar, diríjase a la terminal y ejecute el comando.

.. code-block:: text

 $ virt-manager

Esto iniciará la aplicación GUI del administrador de máquinas virtuales como se muestra.


.. image:: /images/virt-manager.png

Para comenzar a crear una máquina virtual, haga clic en el icono ' Nueva máquina virtual ' en la esquina superior izquierda, justo debajo del elemento de menú ' Archivo '.

.. image:: /images/icono.png

El siguiente paso presenta una lista de opciones entre las que puede elegir al seleccionar su sistema operativo preferido.

* La primera opción - Medios de instalación local (imagen ISO o CDROM) - le permite seleccionar una imagen ISO en su sistema local o seleccionar un sistema operativo desde una unidad de CD o DVD insertada.
* La segunda opción, Instalación de red (HTTP, FTP o NFS) , le permite seleccionar una imagen ISO en la red. Para que esto funcione, la imagen ISO debe montarse en un servidor web, servidor FTP o sistema de archivos de red. Tenemos una guía completa sobre "cómo implementar una máquina virtual en la red usando HTTP, FTP y NFS". (en desarrollo)
* La tercera opción, Network Boot (PXE) , permite que la máquina virtual se inicie desde la tarjeta de red.
* Y la cuarta opción, Importar imagen de disco existente , le permite generar una máquina virtual a partir de una imagen virtual KVM existente.

Asegúrese de seleccionar la opción que más le convenga.

.. image:: /images/create.png


A continuación, haga clic en el botón ' examinar local ' y seleccione la imagen de su disco.

.. image:: /images/examin}.png


El siguiente paso, especifique el tamaño de la RAM y la cantidad de núcleos de CPU que se asignarán y haga clic en ' Adelante '.

.. image:: /images/cpu.png


En el último paso, proporcione el nombre preferido de la máquina virtual y confirme que todos los demás detalles de la máquina virtual están bien. Además, puede optar por configurar las preferencias de red.

.. image:: /images/xd.png
