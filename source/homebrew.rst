.. _homebrew:

Homebrew
========

`Homebrew <https://brew.sh>`__ is a package manager, primarily for MacOS. What
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
installing Homebrew. 

Further documentation about Homebrew and its dependencies is available on the
`Homebrew website <https://brew.sh>`_.

.. container:: vimeo

    .. raw:: html

        <iframe src="https://player.vimeo.com/video/458330008" frameborder="0" allow="autoplay; fullscreen"
        allowfullscreen></iframe>
