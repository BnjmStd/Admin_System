How To Install a Virtual Machine
================================

KVM – Kernel Virtual Machine
-----------------------------

Una máquina virtual basada en el kernel (KVM) es una tecnología de virtualización open source
integrada a Linux®. En concreto, con las KVM puede convertir a Linux en un hipervisor que
permite que una máquina host ejecute varios entornos virtuales aislados llamados máquinas
virtuales (VM) o guests.

Dado que las KVM forman parte del código actual de Linux, aprovechan de forma inmediata todas
sus mejoras, correcciones y funciones nuevas, sin requerir ningún tipo de ingeniería adicional.


Step 1: Check Virtualization Support in Ubuntu
-----------------------------------------------

Para verificar si su sistema admite la virtualización KVM, ejecute el comando:

.. code-block:: text

  $ sudo kvm-ok


Si la utilidad “kvm-ok” no está presente en su servidor, instálela ejecutando el comando apt:

.. code-block:: text

  $ sudo apt install cpu-checker


Ahora ejecute el comando "kvm-ok" para sondear su sistema.

.. code-block:: text

  $ sudo kvm-ok

Virt-Manager
-------------

La aplicación virt-manager es una interfaz de usuario de escritorio para administrar máquinas virtuales a través de libvirt.
Se dirige principalmente a máquinas virtuales KVM , pero también administra Xen y LXC (contenedores Linux).
Presenta una vista resumida de los dominios en ejecución, su rendimiento en vivo y las estadísticas de utilización de recursos.
Los asistentes permiten la creación de nuevos dominios y la configuración y el ajuste de la asignación de recursos y el hardware virtual de
un dominio. Un visor de cliente VNC y SPICE incorporado presenta una consola gráfica completa para el dominio invitado.


libvirt
--------

La biblioteca libvirt se utiliza para interactuar con diferentes tecnologías de virtualización. Antes de comenzar con libvirt, es mejor asegurarse de que su hardware sea compatible con las
extensiones de virtualización necesarias para KVM.


.. code-block:: text

 $ sudo apt update

.. code-block:: text

 $ sudo apt install qemu-kvm libvirt-daemon-system

Step 2: How to install Virt-Manager
-------------------------------------

Antes de continuar, debemos confirmar que el demonio de virtualización, libvritd-daemon, se está ejecutando. Para hacerlo, ejecute el comando.

.. code-block:: text

 $ sudo systemctl status libvirtd

Luego, instalamos virt-manager:

.. code-block:: text

 $ sudo apt install virt-manager



Step 3: Create a virtual machine
---------------------------------

La utilidad virt-manager permite a los usuarios crear máquinas virtuales usando una GUI. Para comenzar, diríjase a la terminal y ejecute el comando.

.. code-block:: text

 $ virt-manager
