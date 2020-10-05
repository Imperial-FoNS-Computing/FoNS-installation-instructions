.. _visual-studio-code:

Visual Studio Code
==================


Visual Studio Code, which used to be called VS Code, is an open source Integrated
Development Environment (IDE) produced by Microsoft. An IDE is a bundle of
functionality for programming which includes a very capable text editor along
a terminal and support for revision control, debuggers for different programming
languages and a host of other features. One key advantage of Visual Studio Code
is its "Live Share" feature, which enables multiple programmers at different
locations to edit the same files collaboratively. This is an immense aid to
group work or getting help from the lecturer when you're not physically in the
same room.

Installing Visual Studio Code on Windows
----------------------------------------

Direct download
...............

You can also install the current Visual Studio Code release directly
`from the Microsoft Website
<https://code.visualstudio.com/docs/setup/windows>`__. If you are working on a
machine where you don't have administrator access, then don't try to use the
"system" installer (use the "user" installer or the "zip" file). If you do have
administrator rights on the machine that you are installing on then any of the
options should work.

Software Hub
............

A slightly older version is available on Software Hub under the name "VS Code".
Follow the instructions on `the Imperial Software Hub website
<https://www.imperial.ac.uk/admin-services/ict/self-service/computers-printing/devices-and-software/get-software/software-hub/>`_.
Because this is a slightly older version, and updates come out every month, you
will immediately be prompted to update.

Installing Visual Studio Code on Mac
------------------------------------

HomeBrew
........

If you have :ref:`installed homebrew <homebrew>` then you can install Visual
Studio Code by :ref:`opening a terminal` and running this command:

.. code-block:: console

    $ brew cask install visual-studio-code

If you install using HomeBrew then the terminal command to
launch Visual Studio Code is set up automatically. This means you can launch
Visual Studio Code from the terminal with this command:

.. code-block:: console

    $ code

Direct download
...............

Follow the `official MacOS Visual Studio Code download link
<https://code.visualstudio.com/docs?dv=osx>`_. Rather than an installer, this
directly downloads the program itself. Open up the Finder (press `⌘ + space` and
type `finder` then press `enter` (⏎)) and copy Visual Studio Code from the
Downloads folder to the Applications folder.

If you want to be able to start Visual Studio Code from the :ref:`terminal`,
then you'll need to do a little more setup from inside the program itself,
following the instructions `on the Microsoft Visual Studio Code website
<https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line>`__.

Installing Visual Studio Code on Linux 
--------------------------------------

Microsoft provide Visual Studio Code packages for a number of Linux
distributions. See the `Visual Studio Code Linux installation webpage
<https://code.visualstudio.com/docs/setup/linux>`__.

In particular, for Debian and Ubuntu based distributions, the easiest way to install Visual Studio Code is to download and install the ``.deb`` package (64-bit) from `here <https://code.visualstudio.com/Download>`__, and then through the command line in terminal with:

.. code-block:: console

    $ sudo dpkg -i <file>.deb

Installing the ``.deb`` package will automatically install the apt repository and signing key to enable auto-updating of the software using the system's package manager. 

Customizing Visual Studio Code
------------------------------

Adding Extensions
.................

There are a number of Visual Studio Code `extensions <https://marketplace.visualstudio.com/>`__ specific to certain programming languages, debuggers, and tools such as a Git repositoy controls support your code development. Please `see this webpage <https://code.visualstudio.com/docs/editor/extension-gallery>`__ and `this one <https://code.visualstudio.com/docs/introvideos/extend>`__ (also has a video tutorial) for more information and howto's. 

In particular, you may be interested in the following extensions:

* `Liveshare <https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack>`__ (Real-time collaborative coding)
* `GitLens <https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens>`__ (Add to the inbuilt Visual Studio Code Git capabilities to seamlessly use Git and control Git repositories within the IDE)
* `Prettier <https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode>`__ (To impose consistency in code formattiong)
* `Python language support <https://marketplace.visualstudio.com/items?itemName=ms-python.python>`__
* `R language support <https://marketplace.visualstudio.com/items?itemName=Ikuyadeu.r>`__
* `Path Intellisense <https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense>`__ (Autocomplete directory paths and filenames)

There are scores of other extensions that you might want to try out depending on the programming language or toolset you are using (e.g., `LaTeX Workshop <https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop>`__). 

Sending text to terminal
........................

 Most code editors will disable sending text to an (usually, embedded) terminal for security reasons. To enable this behavior in Visual Studio Code, do the following (its slightly tricky!):

* Enter `ctrl+shift+P` in vscode. This will bring up the command "palette" box at the top of the editor.
* There, search for "keyboard", which will bring up a few options. from the list, open `Preferences:Open Keyboard Shortcuts File` (both are `json <https://en.wikipedia.org/wiki/JSON>`__ files). 
* Place your key bindings in this file to overwrite the defaults (as it says at the top!). Then, add the following to the json file:   

.. code-block:: JSON

    {
      "key": "ctrl+enter",
      "command": "workbench.action.terminal.runSelectedText"
    }

Note that this is a `json` file format; so, each keybinding is in a separate pair of `{ }`'s, each kebinding specification then separated by commas.
