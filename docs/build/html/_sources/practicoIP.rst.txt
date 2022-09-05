Práctico SSH
========================================

Step 0: Obtener privilegios de superusuario
---------------------------------------------


.. code-block:: text

  $ sudo su-


Step 1: Instalar net-tools
---------------------------

.. code-block:: text

  $ apt-get install net-tools

Step 2: Instalar build-essential
---------------------------------

.. code-block:: text

  $ apt-get install build-essential

Step 3: Instalar servidor SSH
---------------------------------

.. code-block:: text

  $ apt install openssh-server

Step 5:  Verificar el estado del servidor
------------------------------------------

.. code-block:: text

  $ systemctl status sshd

Sin embargo, si no se está ejecutando activamente en su sistema, ejecute:

.. code-block:: text

  $ systemctl enable --now sshd


Step 6: Cambiar ip máquina virtual
-----------------------------------

El comando ifconfig en Linux es una herramienta para gestionar la interfaz de red.
Con ifconfig puedes asignar direcciones IP, habilitar o deshabilitar interfaces de red, administrar la caché ARP y mucho más.

.. code-block:: text

  $ ifconfig -a


Como ya conocemos nuestra IP, podemos editar el archivo:

.. code-block:: text

  $ vim /etc/networks/interfaces


Como se observa en la imagen de abajo se agregan valores:

.. image:: /images/practicoIP/ip.png


* Los valores agregados al archivo "interfaces", son a partir de la intrucción del práctico.

Step 7: Crear el puente a la máquina virtual
---------------------------------------------

Como se conoce la ip de nuestra maquina virtual, en nuestra maquina local editaremos el archivo:

.. code-block:: text

  $ vim .ssh/config

.. image:: /images/practicoIP/config.png

Los valores variarán dependiendo los valores ingresados en el archivo:

.. code-block:: text

  $ vim /etc/networks/interfaces
