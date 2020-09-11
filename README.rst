Source for the Imperial College London Faculty of Natural Sciences computational
software installation instructions
=================================================================================

If you are looking for the installation instructions themselves, then you need
to navigate to `the installation instructions site
<https://imperial-fons-computing.github.io>`_.

Contributing to the instructions
--------------------------------

The site is built using `Sphinx <https://www.sphinx-doc.org/en/master/>`, which
is a documentation generation system widely used in the Python community and
beyond. The documentation itself is written in `reStructuredText
<https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_
which is a light-weight mark up language similar to MarkDown. You can contribute
material by forking this repository and creating a pull request.

If you are a FoNS staff member who is going to make larger or more frequent
commits, you can request write access to this repository by contacting `David
Ham <mailto:david.ham@imperial.ac.uk>`_.

Building the website
--------------------

Building the website locally to check your work is usually quite
straightforward. You will need Python and Make. 

Having cloned this repository, you will need the sphinx and sphinx-autobuild
Python packages, which you can install using:

.. code-block:: console

    python3 -m pip install sphinx sphinx-autobuild

You can then build the website locally by typing:

.. code-block:: console

    make html

The website will appear in the `build/html` subdirectory of the repository.
It is frequently more convenient to have Sphinx constantly update the local html
every time you save the document. This can be achieved with:

.. code-block:: console

    make livehtml

This will serve the constantly updated website on `http://localhost:8000`_.
