.. _homebrew:

Homebrew
========

`Homebrew <https://brew.sh>`_ is a package manager, primarily for MacOS. What
this means is that it provides a mechanism for easily installing a wide range of
software packages. This avoids the need to click through a different set of
installation options for each new package. Instead, most packages can be
installed by typing a simple command such as:

.. code-block:: console

    brew install git

or, for graphical packages:

.. code-block:: console

    brew cask install visual-studio-code

You don't strictly need Homebrew in order to install the packages you need to do
your module: you can instead install each one using its graphical install
process. However, you may find it easier to use Homebrew,
particularly if your modules require several packages to be installed.

Installing homebrew
-------------------

`Open a terminal <terminal>`_ and type:

.. code-block:: console

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

This will start the install process, and ask you for confirmation before
installing Homebrew. It's also very likely that some of the packages you will
install will depend on Apple's basic software development kit, the Command Line
Tools for XCode. Type the following to install these:

.. code-block:: console

    xcode-select --install

Further documentation about Homebrew and its dependencies is available on the
`Homebrew website <https://brew.sh>`_.
