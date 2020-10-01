.. jupyter:

Installing Jupyter
------------------

Please see project Jupyter's `instructions for installation
<http://jupyter.readthedocs.io/en/latest/install.html>`__. Basically,

-  **If you already have Python (2 or 3)**, follow the following
   instructions for your particular OS from the above webpage. We will
   use Python 3 henceforth.

-  **If you are a new Python user, or just want to reinstall Python
   (say, to move from Python 2 to 3)** you can install Python+Jupyter
   using `Anaconda <https://www.continuum.io/downloads>`__, by
   downloading Anaconda's latest Python 3 version.

Ubuntu / Linux
~~~~~~~~~~~~~~

As an existing Python 3 user, you may wish to install Jupyter using
Python's package manager, ``pip``, instead of Anaconda. Do the
following:

.. code:: bash

   sudo pip3 install --upgrade pip

   pip3 install jupyter

If pip3 is not available, then first:

.. code:: bash

   sudo apt-get install python3-pip

If you keep getting a ``pip2 command not found`` error:

.. code:: bash

   sudo apt remove python3-pip && sudo apt install python3-pip

..

   If you already have python 2.x and then installed python3, your pip
   will be pointing to pip3. you can verify that by typing
   ``pip --version`` which would be the same as ``pip3 --version``.

Python 2.7 on Ubuntu 16.04
^^^^^^^^^^^^^^^^^^^^^^^^^^

If this does not work for python 2.7 on Ubuntu 16.04, do this:

.. code:: bash

   sudo apt-get update

   sudo apt-get -y install python2.7 python-pip python-dev

   python --version

   pip --version

   sudo apt-get -y install ipython ipython-notebook

   sudo -H pip install jupyter

You will likely get an error like: "You are using pip version 8.1.1,
however version 8.1.2 is available."

.. code:: bash


   sudo -H pip install --upgrade pip

   sudo -H pip install jupyter

Mac
^^^

.. code:: bash

   pip3 install --upgrade pip

   pip3 install jupyter

Windows
^^^^^^^

Best option is to download and install Anaconda:
https://www.continuum.io/downloads


Installing Language Kernels
~~~~~~~~~~~~~~~~

The Jupyter notebook can support almost `100 programming
languages <https://github.com/jupyter/jupyter/wiki/Jupyter-kernels>`__
(and counting).

The IPython kernel
^^^^^^^^^^^^^^^^^^

The default kernel you will have is IPython (with Python 3 or 2) – the
core Jupyter kernel. Click on the kernel menu item at the top of your
notebook to check.

If you upgraded to Python 3 from 2 **after** installing Jupyter, you
will need to reinstall Jupyter using ``pip``:

.. code-block:: console

    $ sudo pip install jupyter

You will then need to relaunch Jupyter. You should see the Python 3
kernel. If you want both Python 2 and 3 kernels, `see
this <https://stackoverflow.com/questions/30492623/using-both-python-2-x-and-python-3-x-in-ipython-notebook>`__.

The R kernel
^^^^^^^^^^^^

Let's add the R kernel as well. First have a quick look at the `Jupyter kernel
documentation <http://jupyter.readthedocs.io/en/latest/projects/kernels.html>`__
.

Now, go to the `IRKernel github <https://github.com/IRkernel/IRkernel>`__, and
follow the instructions for installing using the ``devtools`` package in R (This
package will also soon be installable through CRAN).


      *On Ubuntu 20.04, If you run into errors while installing the  ``devtools`` package through R, very likely you might need to install the ``curl`` package using ``sudo apt-get install`` in a terminal first (read the error messages you get in R).*

After installing the R kernel, relaunch Jupyter as you did above, and
then check your kernels in the drop-down Jupyter nb menu – you should
now have both Python and R.

Adding extensions to Jupyter
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can add some useful additional functionalities to your Jupyter
notebook interface using (the unofficial)
`extensions <https://github.com/ipython-contrib/jupyter_contrib_nbextensions>`__.
The list of extensions and further instructions for installation can be
`found
here <http://jupyter-contrib-nbextensions.readthedocs.io/en/latest/>`__.
You will also probably want to install the `extensions
"configurator" <https://github.com/Jupyter-contrib/jupyter_nbextensions_configurator>`__.
This package will add useful functionalities like :math:`\LaTeX`
environments and TOCs.

Resources
~~~~~~~~~

-  Check out...