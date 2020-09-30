SSH
===

SSH, the Secure SHell is a program which enables you to connect to another
computer to run commands in a :ref:`terminal <terminal>`. Other programs can
also run over the SSH connection, so SSH can also be used for tasks like copying files between
computers or to enable :ref:`Visual Studio Code` to open files located on a
different computer. 


Installing SSH on Windows
-------------------------

Windows doesn't come with SSH installed, but it does come with the Windows
installation of Git. So if you have :ref:`installed
Git <git-windows>` then you will have ssh installed.

Alternatively, you can install SSH by :ref:`opening Powershell
<terminal-windows>` and typing:

.. code-block:: console

    > Add-WindowsCapability -Online -Name OpenSSH.Client*

SSH on Mac
----------

All recent versions of MacOS come with ssh installed. 

SSH on Linux
------------

SSH is usually installed on Linux machines by default. In the unlikely event
that it's not installed, it will be available using your distribution's package
manager. For example on Ubuntu and related distributions, you would type:

.. code-block:: terminal

    $ sudo apt install ssh-client
