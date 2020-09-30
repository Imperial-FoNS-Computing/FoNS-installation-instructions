R and RStudio
=============

R is a high-level interpreted programming language used in many modules with a
statistical component. RStudio is an integrated development environment (IDE)
for R, providing editing, debugging and much more.

Installing R and RStudio on Windows
-----------------------------------

Software Hub
~~~~~~~~~~~~

Navigate to the `Software Hub <https://softwarehub.imperial.ac.uk/>`__, scroll
down to RStudio (or type it in the search box) and click `Launch`. The RStudio
on Software Hub also includes R so you don't need to install it separately.

Further information on using the Software Hub is available on the `Imperial ICT
Software Hub webpage <https://www.imperial.ac.uk/admin-services/ict/self-service/computers-printing/devices-and-software/get-software/software-hub/>`__.

Direct install
~~~~~~~~~~~~~~


Installing R and RStudio on Mac
-------------------------------

Homebrew
~~~~~~~~

The easiest way to install R and RStudio on Mac is to :ref:`install Homebrew
<homebrew>` and then run the following commands :ref:`in the terminal
<terminal-mac>`:

.. code-block:: console

    $ brew cask install r
    $ brew cask install rstudio

Direct install
~~~~~~~~~~~~~~

The current version of R can be obtained from the `Comprehensive R Archive
Network Mac download page <https://cran.r-project.org/bin/macosx/>`__. The click
on the latest release link (it will be called something like R-4.0.2.pkg, but
the version may be newer than that). Run the installer and accept all of the
default options.

RStudio can be installed from the `RStudio install page
<https://rstudio.com/products/rstudio/download/#download>`__. Usually the big
blue button will automatically detect the right version. Again, run the
installer and accept the default options.

Running RStudio
~~~~~~~~~~~~~~~

You launch RStudio by pressing `⌘ + space` to open Spotlight search and
type `rstudio` in the resulting search box:

.. image:: _static/spotlight-rstudio.png
