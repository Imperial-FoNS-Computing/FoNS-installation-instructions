.. _linux:

Obtaining a Linux/Unix environment  
==================================

Unix is a family of operating systems which are widely used in science. In
particular, almost all supercomputers run Linux, which is one of the Unix
operating systems. Unix systems are preferred for many programming tasks, so you
may find it advantageous to have a Unix environment available to you on your
computer.

We recommend Ubuntu as the go to Linux distribution for students and staff as
there is some level of ICT support for it. Advanced users are free to use their
own distribution such as Fedora, Mint, etc.

Obtaining Linux/Unix from Windows 10
------------------------------------

If you have a Windows 10 computer then you have three options for obtaining a
Linux environment:

Windows subsystem for Linux
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Windows subsystem for Linux is the in-built mechanism for obtaining a Linux
environment that runs inside your exising Windows operating system. Follow the
`official Microsoft WSL installation instructions
<https://docs.microsoft.com/en-us/windows/wsl/install-win10>`__. Of the options
on that page, you probably want to choose WSL 2 rather than WSL 1, and you
probably want to install the most recent version of Ubuntu offered.

.. _virtual-machine:

Run Linux in a Virtual machine
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A Virtual Machine is another mechanism for running one operating system inside another
one. Imperial provides licences for VMWare, which is one popular virtual machine
framework. Follow `Imperial's instructions to obtain VMWare <https://www.imperial.ac.uk/admin-services/ict/self-service/computers-printing/devices-and-software/get-software/get-software-for-students/vmware/>`__.

Once you have VMWare, you will need to create a virtual machine running Ubuntu
(or whichever other host operating system you want). There are many tutorials on
this all over the web. For example you might follow this `tutorial on installing
Ubuntu on VMWare <https://linuxhint.com/install_ubuntu_vmware_workstation/>`__. 

Install Linux alongside or instead of Windows
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This option involves natively installing Linux on your computer so it runs by
itself and not within Windows. You can either remove Windows completely and
always run Linux as the primary OS, or you can set your computer up with both
operating systems on the hard drive so that you can choose to boot into either.
This is called a dual-boot configuration. Follow the :ref:`instructions for natively
installing Linux <install-linux>` below.

Mac is Unix
-----------

Both Linux and MacOS operating systems are members of the  Unix family of
operating systems. MacOS is based on Darwin (a unix-like operating
system), whilst Linux is another Unix-like OS.
 
Practically this means that MacOS and Linux behave similarly and are both much
easier to program with than Windows. That said, there are some benefits to Linux
for a programmer over MacOS. Firstly you are basically trusted to break and fix
most things yourself, whilst you CAN do similar things on Mac, they may be
harder to achieve or done in different, more roundabout ways.
 
There are minor inconsistencies between Mac and Linux implementations of various
tools, for instance ``grep``. This means that a bash script written for Linux
may not work out of the box on Mac. But that is a minor issue. 

So the take-home message is, don't bother with a MacOS - Linux dual
boot, unless your life is *really* boring. If you particularly do need an actual
Linux environment under MacOS, then the :ref:`instructions for installing a virtual
machine <virtual-machine>` will also work for Mac.

.. _linux-chrome:

Activating Linux on Chrome OS
-----------------------------

Recent Chromebooks have a built-in ability to run Linux in a virtual machine.
This is important since many of the programming tools required for Faculty of
Natural Sciences cannot be installed natively on ChromeOS, but can be installed
in the Linux virtual machine. Follow the `instructions for setting up Linux on
your Chromebook <https://support.google.com/chromebook/answer/9145439>`__

Once you have done this, you will have a Debian Linux installation set up inside
Chrome OS. Debian is a very close relative of Ubuntu so the installation
instructions provided for various packages for Ubuntu will probably work for you.

.. _install-linux:

Installing Ubuntu Linux
-----------------------

You may already have (or received) a bootable USB stick with Ubuntu 20.04 (64
bit) installer on it. If you didn't or would rather make your own (indeed, why
not?!), `its pretty easy
<https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0>`__.

Ubuntu-only install
~~~~~~~~~~~~~~~~~~~

Once you have your bootable USB, `follow this
tutorial <https://tutorials.ubuntu.com>`__. The best way to do this is
to keep it handy on your smart phone or another computer and go through
the process.

Basically, you need to boot your computer from the Ubuntu USB. Many
computers will boot from (a bootable) USB stick automatically. Simply
insert the USB flash drive and either power on your computer or restart
it. You should see the Ubuntu welcome window from where you can install
Ubuntu desktop.

If your computer doesn't automatically boot from USB, try holding
``F12`` when your computer first starts. With most machines, this will
allow you to select the USB device from a system-specific boot menu. If
``F12`` does not bring up your system's boot menu, Escape, F2 and F10
are common alternatives. Otherwise, just `check this
webpage <http://www.disk-image.com/faq-bootmenu.htm>`__. You can also
look for a brief message when your system starts, that will tell you
which key to press to bring up the boot menu.

Once you have the Ubuntu welcome screen, the rest should be easy. If you intend
to install Ubuntu as the only operating system on your system then choose
“Erase disk and install Ubuntu” option.

Dual boot with Windows
~~~~~~~~~~~~~~~~~~~~~~

You can also set up your computer to dual boot Ubuntu and Windows.

There are few (no?) benefits to choosing to dual-boot, and we do not
recommended it. One reason may be that you are using your own laptop,
and are keen on keeping your Windows. In that case, try it. `There are detailed instructions
available <https://help.ubuntu.com/community/WindowsDualBoot>`__.

Alternatively, do a native install of Ubuntu, and then virtualize the
other operating system. Google "windows virtual machine on ubuntu", and
you will get plenty of step by step tutorials.

Creating partitions during Linux installation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

When you install Ubuntu, you will have the opportunity to create separate
``swap``, ``root`` and ``home`` partitions on your hard disk. ``swap``
necessarily needs to be a separate partition, while ``root + home`` can be on
the same partition. 

We suggest that you create a separate ``home`` partition, even though it is not
necessary — that way, even if you break your linux install, you can easily
reinstall it by just wiping the root partition, without losing any of your data
(which sits in ``home``).

If you are unsure about this, just go with the default, or ask one of your instructors/GTAs.

Tweaking your Ubuntu OS
-----------------------

Once you have installed Ubuntu, there are are many ways in which you can
tweak your OS environment. For example, see
http://www.howtogeek.com/tag/ubuntu/ubuntu-tips/.

But be careful, it can be addictive and dangerous to your system's
stability!

Here are a couple of tweaks to our bash/terminal behavior that are
recommended.

Opening Nautilus from terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In terminal you can simply enter “f” to open nautilus in current
directory by doing the following. Firstly make a ``.bash_aliases`` file,
then open it for editing:

.. code-block:: console

    $ touch ~/.bash_aliases
    $ gedit ~/.bash_aliases

Next add to the last line of the file, add:

.. code-block:: console

    $ alias f='nautilus . &'

Then restart terminal, or in current terminal, type:

.. code:: bash

    source ~/.bash_aliases

Enabling auto-complete in terminal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

What happens when you use up and down keys in terminal? If nothing, then
you need to enable reverse searching history. To do so, open
``/etc/inputrc`` for editing:

.. code:: bash

    sudo gedit /etc/inputrc

Then, add the following to it:

.. code:: bash

   ## arrow up
   "\e[A":history-search-backward
   ## arrow down
   "\e[B":history-search-forward

That's it. Now when you type part of a command that you have used in the
past and then press the up key, it will autocomplete by
reverse-searching history (open a new terminal and try it!).

Resources
---------

-  `Ubuntu tutorials <https://tutorials.ubuntu.com/>`__
-  `Bootable USB
   tutorial <https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-ubuntu#0>`__
-  `Installation
   tutorial <https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview>`__