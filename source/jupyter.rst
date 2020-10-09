.. _jupyter:

Jupyter
=======

There are currently `two options
<https://jupyter.readthedocs.io/en/latest/index.html>`__ for Jupyter that are
relevant here: the "classic" Jupyter notebook interface, and JupyterLab, the
next-generation user interface for the Jupyter Project. Jupyterlab has a modular
structure, where you can open several notebooks or files (e.g. HTML, Text,
Markdowns etc) as tabs in the same window, and basically offers more of an `IDE
<https://en.wikipedia.org/wiki/Integrated_development_environment>`__-like
experience.

JupyterLab is fast evolving, and will likely replace Jupyter sooner than later. 

We suggest installing both, the classic Jupyter Notebook and Jupyter Lab, as there are certain extensions in the former, such as the nifty `RISE extension <https://rise.readthedocs.io/en/stable/index.html>`__,  that are not yet compatible with the latter. 

Installing
----------

Please see project Jupyter's `instructions for installation
<http://jupyter.readthedocs.io/en/latest/install.html>`__, which covers both  Jupyter variants. 

Basically,

-  **If you already have Python 3**, follow the following
   instructions for your particular OS from the above webpage. We will
   use Python 3 henceforth.

-  **If you are a new Python user, or just want to reinstall Python
   (say, to move from Python 2 to 3)** you can install Python+Jupyter
   using `Anaconda <https://www.continuum.io/downloads>`__, by
   downloading Anaconda's latest Python 3 version.

Windows
~~~~~~~

Your best option is to download and :ref:`install Anaconda <python>`, which
includes Python and Jupyter Notebook (among other useful pckages and utilities).

Mac
~~~

Your best option is to download and :ref:`install Anaconda <python>`, which
includes Python and Jupyter Notebook (among other useful pckages and utilities).

Linux or Chrome OS [#Chrome]_
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you are an an existing Python 3 user, instead of Anaconda, you may wish to install Jupyter using the Python package manager `pip` , with:

.. code:: console

   $ python3 -m pip install jupyter
   $ python3 -m pip install jupyterlab

If pip is not available, then :ref:`see this <python>`.

Language Kernels
----------------

The Jupyter notebook can support almost `100 programming languages
<https://github.com/jupyter/jupyter/wiki/Jupyter-kernels>`__ (and counting). We will describe the installation of two (IPython and R) because these are likely to be used most commonly across courses. 

The IPython kernel
~~~~~~~~~~~~~~~~~~

The default kernel you will have is IPython (with Python 3 or 2) – the core
Jupyter kernel. Click on the kernel menu item at the top of your notebook to
check.

If you upgraded to Python 3 from 2 **after** installing Jupyter, you will need
to reinstall Jupyter using `pip`:

.. code-block:: console

   $ python3 -m pip install jupyter

You will then need to relaunch Jupyter. You should see the Python 3 kernel. If
you want both Python 2 and 3 kernels, `see this
<https://stackoverflow.com/questions/30492623/using-both-python-2-x-and-python-3-x-in-ipython-notebook>`__.

The R kernel
~~~~~~~~~~~~

First have a quick look at the `Jupyter kernel documentation
<http://jupyter.readthedocs.io/en/latest/projects/kernels.html>`__ .

Now, go to the `IRKernel github <https://github.com/IRkernel/IRkernel>`__, and
follow the instructions for installing using the `devtools` package in R (This
package will also soon be installable through CRAN).

On Ubuntu 20.04, If you run into errors while installing the  `devtools` package through R, very likely you might need to install the `curl` package using `sudo apt install` in a terminal first (read the error messages you get in R).

After installing the R kernel, relaunch Jupyter as you did above, and
then check your kernels in the drop-down Jupyter nb menu – you should
now have both Python and R.

Adding extensions
-----------------

You can add some useful additional functionalities to your Jupyter notebook
interface using (the unofficial) `extensions
<https://github.com/ipython-contrib/jupyter_contrib_nbextensions>`__. The list
of extensions and further instructions for installation can be `found here
<http://jupyter-contrib-nbextensions.readthedocs.io/en/latest/>`__. You will
also probably want to install the `extensions "configurator"
<https://github.com/Jupyter-contrib/jupyter_nbextensions_configurator>`__. This
package will add useful functionalities like :math:`\LaTeX` environments and
TOCs.

.. rubric:: Footnotes

.. [#Chrome] To use these installation instructions for Chrome OS you first need to :ref:`set up Linux on your Chromebook <linux-chrome>`.
