LaTeX
=====

LaTeX is a typesetting system which is widely used by scientists, and especially
mathematicians, in preference to word processors.

Overleaf
--------

One of the easiest ways to use LaTeX is through the cloud service Overleaf. This
gives you a fully featured LaTeX system in your web browser without installing anything.
Imperial has a professional licence for Overleaf which will cover you if you
register using your Imperial email address. `Register for Overleaf here
<https://www.overleaf.com/register>`__.

Installing LaTeX on Windows
---------------------------

Software Hub
~~~~~~~~~~~~

You can install the MikTeX distribution of LaTeX by navigating to `the Software
Hub <softwarehub.imperial.ac.uk>`__ and launching TexMaker. Further information
on using the Software Hub is available on the `Imperial ICT Software Hub webpage
<https://www.imperial.ac.uk/admin-services/ict/self-service/computers-printing/devices-and-software/get-software/software-hub/>`__.

Direct install
~~~~~~~~~~~~~~

The MikTeX distribution has step by step installation instructions on `the
MikTeX Windows Installation website <https://miktex.org/howto/install-miktex>`__.

Installing LaTeX on Mac
-----------------------

Homebrew
~~~~~~~~

If you've :ref:`installed Homebrew
<homebrew>` then you can install the MacTeX distribution of LaTeX by :ref:`opening a terminal
<terminal-mac>` and running the following command:

.. code-block:: console

    $ brew cask install mactex

Direct install
~~~~~~~~~~~~~~

Head to the `MacTeX website
<http://www.tug.org/mactex/mactex-download.html>`__ and follow the instructions
there.

Installing LaTeX on Linux
-------------------------

All of the LaTeX distributions ship LaTeX via their package manager. LaTeX is
very large, so often the distributions will split it into several packages and
you may find yourself needing to install additional packages as you use more
LaTeX features.

For Ubuntu you can get a fairly complete LaTeX install by running the following
in the :ref:`terminal <terminal>`.

.. code-block:: console

    $ sudo apt-install texlive-latex-extra

For Fedora, you would run:

.. code-block:: console

    $ sudo dnf install texlive-scheme-medium

More details can be found on the `Fedora LaTeX website
<https://docs.fedoraproject.org/en-US/neurofedora/latex/>`__.
