.. linux:

Installing Linux  
================

We recommend Ubuntu as the go to Linux distribution for students and staff as
there is some level of ICT support for it. Advanced users are free to use their
own distribution such as Fedora, Mint, etc. 

Installing Ubuntu
-----------------

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

Once you have the Ububtu welcome screen, the rest should be easy. If you
are using one of the College-issued CMEE laptops, you should choose the
“Erase disk and install Ubuntu” option.

Dual boot with Windows
~~~~~~~~~~~~~~~~~~~~~~

You can also set up your computer to dual boot Ubuntu and Windows.

There are few (no?) benefits to choosing to dual-boot, and we do not
recommended it. One reason may be that you are using your own laptop,
and are keen on keeping your Windows installation that you paid $$ or
$$$$ for. In that case, try it. `There are detailed instructions
available <https://help.ubuntu.com/community/WindowsDualBoot>`__.

Alternatively, do a native install of Ubuntu, and then virtualize the
other operating system. Google "windows virtual machine on ubuntu", and
you will get plenty of step by step tutorials.

Dual boot with Mac OS
~~~~~~~~~~~~~~~~~~~~~

Don't be crazy! 

Both Linux and MacOS operating systems stem from Unix, an older OS which was fairly heavily copyrighted and licensed. MacOS is based on Darwin (a unix-like operating system), whilst Linux is another Unix-like OS.
 
Practically this means that MacOS and Linux behave similarly and are both much easier to program with than Windows. That said, there are some benefits to Linux for a programmer over MacOS. Firstly you are basically trusted to break and fix most things yourself, whilst you CAN do similar things on Mac, they may be harder to achieve or done in different, more roundabout ways.
 
There are minor inconsistencies between Mac and Linux implementations of various tools, for instance ``grep``. This means that a bash script written for Linux may not work out of the box on Mac. BUt that is a minor issue. 

So the take-home message is, don't bother wasting time with a MacOS - Linux dual boot, unless your life is *really* boring. 


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