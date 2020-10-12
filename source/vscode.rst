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
Studio Code by :ref:`opening a terminal <terminal-mac>` and running this command:

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
directly downloads the program itself. Open up the Finder (press :kbd:`⌘` + :kbd:`space` and
type `finder` then press :kbd:`enter` (:kbd:`⏎`)) and copy Visual Studio Code from the
Downloads folder to the Applications folder.

If you want to be able to start Visual Studio Code from the :ref:`terminal`,
then you'll need to do a little more setup from inside the program itself,
following the instructions `on the Microsoft Visual Studio Code website
<https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line>`__.

Installing Visual Studio Code on Linux or Chrome OS [#Chrome]_
--------------------------------------------------------------

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
* `Prettier <https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode>`__ (To impose consistency in code formatting)
* `Python language support <https://marketplace.visualstudio.com/items?itemName=ms-python.python>`__
* `R language support <https://marketplace.visualstudio.com/items?itemName=Ikuyadeu.r>`__
* `Path Intellisense <https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense>`__ (Autocomplete directory paths and filenames)

There are scores of other extensions that you might want to try out depending on the programming language or toolset you are using (e.g., `LaTeX Workshop <https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop>`__). 

Sending text to terminal
........................

 Most code editors will disable sending text to an (usually, embedded) terminal for security reasons. To enable this behaviour in Visual Studio Code, do the following (its slightly tricky!):

* Press :kbd:`control` + :kbd:`shift` + `P` in vscode. This will bring up the command "palette" box at the top of the editor.
* There, search for "keyboard", which will bring up a few options. from the list, open `Preferences:Open Keyboard Shortcuts File` (both are `json <https://en.wikipedia.org/wiki/JSON>`__ files). 
* Place your key bindings in this file to overwrite the defaults (as it says at the top!). Then, add the following to the json file:   

.. code-block:: JSON

    {
      "key": "ctrl+enter",
      "command": "workbench.action.terminal.runSelectedText"
    }

Note that this is a `json` file format; so, each keybinding is in a separate pair of `{ }`'s, each keybinding specification then separated by commas.

Live Share
----------

One of the key advantages of Visual Studio Code is its Live Share extension.
Live Share enables two or more programmers to each run Visual Studio Code on
their own computers but to see and edit the same files in real time, and to see
each other's cursors as they edit. Live Share can make collaboration much
easier, and it also facilitates remote computer lab sessions: the remote
equivalent of having an instructor look over your shoulder at the screen is to
Live Share your session with them. Live Share takes a lot less bandwidth than
sharing your screen and because each participant uses their own IDE, they can
independently set factors such as the font size to settings that are legible for
them. There is also a Live Share Audio extension that enables you to talk with
your collaborators, though you can also use a simultaneous call on another
platform such as MS Teams or Zoom.

.. warning: Live Share does not share Jupyter notebook sessions.

    The current (as of October 2020) Live Share capabilities of Visual Studio
    Code do not extend to sharing Jupyter notebook sessions. If you need to
    share a Jupyter notebook session then you currently need to share your
    screen using, for example, MS Teams.

Installing the Live Share extension
...................................

Click on the extensions icon, |extension|, in the left hand bar in Visual Studio
Code. In the search box which appears, type `Live Share` then :kbd:`enter`.
Click on the `install` button under the `Live Share` extension. Once the
extension is installed, you should see |liveshare| at the bottom of your Visual
Studio Code screen.

Starting a Live Share
.....................

Using Live Share requires that you log in using either a Microsoft or a GitHub
account. If you have neither, then :ref:`follow these instructions to sign up to
GitHub <github_signup>`. Next click on |liveshare| and sign in when prompted.
Once you have signed in, you will see the following:

.. image:: _static/vscode_start_liveshare.*

At this stage, the Live Share link has been copied to your clipboard. To invite
someone else to join your session, you just need to provide them with this link.
For example you could email it to them, or paste it into a chat message. You
also have the opportunity at this stage to switch the session to read only,
which means that your collaborator will be able to see your session but not edit
your files.

Joining a Live Share
....................

If a collaborator passes you a Live Share link then you can usually simply click
on it. This will open a web browser and, assuming you have Visual Studio Code
installed, the browser will ask you if you want to open Visual Studio Code. You
should agree. Alternatively, if you don't have Visual Studio Code installed,
you can click on the link to join from your browser. If you do have Visual
Studio Code installed but are not prompted to join the session live, then you
can follow the link to join manually, which will give you instructions as to
where to paste the link in Visual Studio Code itself.

Participating in a Live Share
.............................

All participants in a Live Share can see all the files in the project, and each
others cursors. If there Live Share permits editing (the default), then all
participants can also edit the files. The image below shows a Live Share session
in progress. The local user's cursor is visible in grey while the remote
participant's is orange:

.. image:: _static/vscode_participate_liveshare.*

The other new image on the screen is the little pin at top right: |pin|. When
this pin is selected, it turns green and indicates that this user is following
the other participant. This means that as the other participant navigates from
around the file or changes files, the display will jump around to follow them.
If there are multiple participants, then you will be asked which participant to
follow.

Sharing a terminal
..................

By default, any :ref:`terminals <terminal-vscode>` that you have running from
within Visual Studio code will not be shared. However, you can launch a shared
terminal that your collaborators can see and (if you allow it) type in. Click on
your name at the bottom of the Visual Studio Terminal and choose `Share Terminal`:

.. image:: _static/vscode_share_terminal.*

On the next page you can choose whether the other participants should be able to
type into the terminal (read/write) or should only be able to watch your work.

Ending the Live Share session
.............................

If you are the host of a Live Share, then you can end the session by clicking on
the Live Share icon on the left, |liveshare_icon|, and then selecting the stop
icon, |liveshare_stop|, which appears when you hover your mouse over the
`SESSION DETAILS` bar: 

.. image:: _static/vscode_stop_liveshare.*

If you are another participant in a live share, just close the Visual Studio
Code window for the Live Share session.

Further documentation on Live Share
...................................

Microsoft publishes extensive documentation and tutorials about how to use Live
Share on the `Visual Studio Live Share website <https://docs.microsoft.com/en-us/visualstudio/liveshare/>`__.

.. |extension| image:: _static/vscode_extension.*
    :height: 2ex

.. |liveshare| image:: _static/vscode_liveshare.*
    :height: 2ex

.. |pin| image:: _static/vscode_pin.*
    :height: 2ex

.. |liveshare_icon| image:: _static/vscode_liveshare_icon.*
    :height: 2ex

.. |liveshare_stop| image:: _static/vscode_liveshare_stop.*
    :height: 2ex



.. rubric:: Footnotes

.. [#Chrome] To use these installation instructions for Chrome OS you first need to :ref:`set up Linux on your Chromebook <linux-chrome>`.
