Práctico
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

Step 7: Crear el puente a la máquina virtual
---------------------------------------------
