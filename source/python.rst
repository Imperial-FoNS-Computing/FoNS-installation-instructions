Python
======

Python is an interpreted high-level programming language used in many modules
with a numerical computing component. There are several ways to install Python
on your computer, but most modules will assume that you are using the Anaconda
distribution, so that's the one whose installation we primarily document here.
If you have another Python 3 distribution installed, then this is likely to
work, however your mechanism for installing additional Python packages may not
be the same as that documented in the lecture materials, so you may have to sort
that out for yourself.

Python 2 and Python 3
---------------------

Python has just completed a decade-long major version transition from Python 2
to Python 3. As of 1 January 2020 Python 2 is officially unsupported, even for
critical security updates. The instructions here are for the installation of
Python 3. Don't try to use Python 2 for your work as it is unsupported and
increasingly likely to have breakages which won't be fixed.

Installing Python in Windows
----------------------------


You can obtain Anaconda `using the Anaconda Windows installation site
<https://docs.anaconda.com/anaconda/install/windows/>`__. Simply follow the
instructions there to download and run the installer.

Installing Python on Mac
------------------------

Homebrew install Anaconda
.........................

If you've installed :ref:`homebrew` then you can install Anaconda by 
to :ref:`opening a terminal <terminal>` and run the following command:

.. code-block:: console

    $ brew cask install anaconda

When asked, enter your Mac password. On this occasion we're not quite done
because Homebrew is quite conservative about installing a new Python over
another one you might have installed. We're going to need to tell the terminal
that we want Anaconda to be our default Python.

The way we do this depends slightly on which command line program (or "shell")
we are using. The default on recent MacOS is `zsh`, but if you've been using
MacOS for a while and haven't changed, you might be using `bash`. Just to be on
the safe side, we'll run both commands. If you know for sure which shell you are
using, then you can just run the appropriate one. If you're not sure, run both:

.. code-block:: console

    $ echo 'export PATH=/usr/local/anaconda3/bin:$PATH' >> ~/.zshrc
    $ echo 'export PATH=/usr/local/anaconda3/bin:$PATH' >> ~/.bash_profile

Then close the terminal and open a new one to make sure the changes have taken
effect. Run the following command to check that Anaconda is working properly:

.. code-block:: console

    $ conda --version
    conda 4.8.3

Don't worry if the version you see installed is not the same as that listed here.

Download and install Anaconda
.............................

You can also install Anaconda on your Mac by downloading the Anaconda installer
and installing it yourself. This is documented on `the Anaconda MacOS
installation website <https://docs.anaconda.com/anaconda/install/mac-os/>`_.

Homebrew Python
...............

An alternative to using Anaconda is to install Python directly using
:ref:`Homebrew <homebrew>`. Simply run:

.. code-block:: console

    $ brew install python

This will automatically ensure that the command `python3` points to the correct
Python installation, however the Python package installation mechanism won't be
the Anaconda one. Instead you will use Python's standard package installer
`pip`. For example if you need to install `numpy` and `matplotlib` (the core
numerical computing and plotting packages), as well as support for Jupyter
notebook, you would run:

.. code-block:: console

    $ pip3 install numpy matplotlib jupyter

.. warning::

    MacOS also comes with Python pre-installed. However this is a very cut-down
    version which is really only intended for internal use by the operating system.
    You should install a fully-featured Python (i.e. Anaconda or Homebrew).

Installing Python on Linux
--------------------------

Every Linux distribution distributes a fully-featured Python, and this might
well be enough for your needs. However if you would prefer to have the same
Python distribution as most of your classmates, then there are instructions for
installing Anaconda on `the Anaconda Linux install website <https://docs.anaconda.com/anaconda/install/linux/>`_.

Installing Python packages on Linux
...................................

If you're using the system Python, as opposed to Anaconda, then you'll use the
Python package manager `pip` to install any additional packages that you need.
There are a couple of issues with this of which you should be aware. First, not
all Linux distributions install `pip` by default, often you need to install an
additional package called something like `python-pip`. For example, on Ubuntu
you would run:

.. code-block:: console

    $ sudo apt-get install python-pip

While on Fedora and related distributions, you would run:

.. code-block:: console

    $ sudo dnf install python-pip

It's also possible to install quite a lot of Python packages using the Linux
package manager in a similar way. However, you will probably want to install at
least some packages using pip. For example if you wanted to install Jupyter you
would type:

.. code-block:: console

    $ pip3 install --user jupyter

The `--user` option tells pip to just install for the current user. This is
preferable to using `sudo` and to install packages globally, as it removes any
risk of interfering with packages that the operating system needs.

