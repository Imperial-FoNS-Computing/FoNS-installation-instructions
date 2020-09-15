Git and GitHub Classroom
========================

Introduction
------------

`Git <https://git-scm.com>`_ and `GitHub <https://github.com>`_ Classroom are
used in some modules to distribute programming coursework, enable you to manage
your code while completing the exercises, and then to help with submission.

.. note::

    This introduction just provides enough information to enable you to set up
    and use Git and GitHub Classroom for your coursework. For a more in-depth
    introduction to Git and GitHub, you are encouraged to work through the
    excellent `Git tutorial provided by the Software Carpentry project
    <http://swcarpentry.github.io/git-novice/>`_.
    
What is Git?
~~~~~~~~~~~~

When we're writing code, we typically don't just type it out, notice that it
works, and stop. Instead, the usual cycle looks a bit more like this:

1. Write a small piece of code.
2. Use it to run some test problems to see if it works.
3. If there were problems, make a change and go back to step 2.
4. Once it's working, go back to step 1 and write the next small piece of code.

Each time we get to step 4, we're a little closer to having a working program
that does what we want. However, each time we go back through steps 1-3, we run
the risk that we don't just implement a new feature, but that in doing so we
break something we already had working. How do we make sure that we always know
exactly what the code used to look like when it worked? 

One answer is to keep saving old versions under different names. This is a bad
answer for two reasons. The first is that it swiftly descends into a confused
mess, as anyone who has ever been emailed a Word file named
`report_draft_final_revised2_johns_comments.doc` can attest! The second is that
the names of files and code objects often matter to programming languages - so
the mere action of saving your code under a different name can stop it working.

The right answer to the problems caused by constantly updating code (or any
other document) is a version control system. A version control system is a piece
of software which keeps track of versions of a collection of files such as a
software project. A well-used revision control system can tell you:

1. What changed in the files.
2. When the change happened.
3. Who made the changes.

Revision control systems also help with the edit conflicts that can occur
when more than one person edits a file, for example as a part of a group
project - or even when you edit the same file on two different computers.

Git is one such revision control system, and it's one of the most capable and
widely used currently available.

What is GitHub?
~~~~~~~~~~~~~~~

Git keeps track of a collection of files stored in a project folder called a
repository which is kept on your computer. That's great but what if you want to
do any of the following?

1. Collaborate with someone else who also needs to edit the files.
2. Work on more than one computer.
3. Still have your repository if your computer is lost or your hard disk dies.

`GitHub <https://GitHub.com>`_ is a cloud service which stores copies of Git
repositories online. You can `push` your changes up to GitHub from any computer
with an internet connection and `pull` those changes down to any other computer.
GitHub also integrates with other software development tools such as automatic
testing frameworks, issue trackers and code review to provide a comprehensive
software development platform. Depending on the module you are taking, you may
also use some of these extra features of GitHub, but we will mostly focus on how
to use the core feature of storing a copy of your repository online.

What is GitHub Classroom?
~~~~~~~~~~~~~~~~~~~~~~~~~

All of the collaborative features of Git and GitHub might sound like overkill
when all you need to do is complete coding assignments that only you work on.
However in software development terms, you always have at least one collaborator
on your assignments: the module lecturer. Usually the lecturer provides some
initial skeleton code, such as some incomplete source files or Jupyter
notebooks. During the course of the work, you might need to show your code to
the lecturer or a teaching assistant in order to get help, and at the end you
need to share your work with the module staff to get it marked.

GitHub Classroom is a service that works with GitHub to provide every student
doing a particular coding exercise with their own repository on GitHub that's
prepopulated with the lecturer's skeleton code and ready to work with. As we'll
see below, this makes it really easy to obtain the exercise and work with it.

Installing Git
--------------

Windows
~~~~~~~

Software Hub
............

Direct download
...............

MacOS
~~~~~

Homebrew
........

If you've :ref:`installed Homebrew <homebrew>` then installing git is as simple
as :ref:`opening a terminal <macos_terminal>` and running the following command:

.. code-block::

    brew install git

Now proceed to :ref:`check the install <macos_check_git>`.

Direct download
...............


.. _macos_check_git:

Check the install
.................

Check that you've got a successfully working Git by running this in the
terminal:

.. code-block:: console

    git --version

The expected output is something like:

.. code-block:: console

    git version 2.28.0

The exact version may be a little different. This is not important.

Proceed now to :ref:`configure Git <configure_git>`.

Linux
~~~~~

Every Linux distribution ships git through its package manager. The easiest way
to install git is usually to simply do whatever it is that is normal on your
distribution to install software. For example on Ubuntu or any other
Debian-based system you would run this in the terminal:

.. code-block:: console

    sudo apt-get install git

While on Fedora and related distributions, you would run:

.. code-block:: console

    sudo dnf install git

or if you're using an older version of these distributions:

.. code-block:: console

    sudo yum install git

If you're using a different Linux distribution then you'll probably find the
correct install line `on the Git Linux download website <https://git-scm.com/download/linux>`_.

Check that you've got a successfully working Git by running this in the
terminal:

.. code-block:: console

    git --version

The expected output is something like:

.. code-block:: console

    git version 2.28.0

The exact version may be a little different. This is not important.

Proceed now to :ref:`configure Git <configure_git>`.

.. _configure_git:

Configuring Git
---------------

Git needs a little bit of configuration to work smoothly. This configuration
belongs to the computer you're running Git on, so you don't have to do this for
each project, but you do have to do it for each computer you log into. If you're
using Imperial's lab machines remotely, these all share user home directories so
you should not need to redo the Git configuration each time you log into a new
lab machine: one configuration is enough for them all.

Your details
~~~~~~~~~~~~

First you need to tell Git about your name and email address. This has nothing
directly to do with the information you provided to GitHub, instead it will just
be used by Git to label you as the author of the code that you write. To save on
a great deal of confusion later, you should register the actual name that you
usually go by. Similarly, please use your Imperial email address. :ref:`Open a
terminal <terminal>` and run the following commands, replacing your name as
appropriate:

.. code-block:: console

    git config --global user.name "Jo Student"
    git config --global user.email "Jo.Student20@imperial.ac.uk"

Line endings
~~~~~~~~~~~~

When a text file, such as a program source file, contains a line break, this is
represented by a special invisible character. Unfortunately, it's not the same
character on different operating systems, which can make a bit of a mess when a
file is created on one operating system, and then edited on another - such as
might happen if your lecturer uses a different operating system for you. We can
set up Git to automatically clean up this mess in most cases.

Windows
.......

Run the following command in the :ref:`Git Bash terminal <terminal>`:

.. code-block:: console

    git config --global core.autocrlf true

MacOS or Linux
..............

Run the following command in the :ref:`terminal <terminal>`:

.. code-block:: console

    git config --global core.autocrlf input

Text editor
~~~~~~~~~~~

Git sometimes needs you to write a text comment. When this is the case, it will
launch a text editor to enable you to type the comment in. If you don't have
strong preferences for a particular editor, then `nano` is a good choice, so run
the following line in the terminal:

.. code-block:: console

    git config --global core.editor "nano -w"

If you have a favourite text editor, you can set it using the `Software
Carpentry instructions
<https://swcarpentry.github.io/git-novice/02-setup/index.html>`_.

Signing up to GitHub
--------------------

You will need your own GitHub account. This is completely
separate from your Imperial College computer account so you need to sign up
separately. If you've already got a GitHub account then you don't need another
one. Assuming you don't already have an account, 
click on `the GitHub signup page
<https://github.com/join?ref_cta=Sign+up>`_.

There are three fields to fill out:

Username
    You can use any name that is not already taken on GitHub. It doesn't need to
    have any relationship to your Imperial account name.

Email Address
    You need to use a real email address that works and you have access to, as
    GitHub will send you a verification email which you need to respond to. It
    is a very good idea to use your Imperial email address as this will make it
    easier to sign up for a GitHub Student Developer Pack (see below).

Password
    Choose a good, secure password. Do **not** use the same password as you use
    for your Imperial computer account.

Obtaining the GitHub Student Developer Pack
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

GitHub provide upgraded "pro" accounts and a bundle of other online tools for
free to students. You don't need this for your Imperial modules, but some of it
may be nice to have if you intend to do more software development as a student.
You can `register for the Student Developer Pack here
<https://education.github.com/pack>`_. Part of the registration is to verify
your student status, and one of the things that GitHub uses for this is your
email address so if you didn't use your Imperial email address to register your
GitHub account, you might want to `add your Imperial email address to your
GitHub account
<https://docs.github.com/en/enterprise/2.15/user/articles/adding-an-email-address-to-your-github-account>`_.

.. _github_classroom_exercise:

Doing coursework using GitHub Classroom
---------------------------------------

Some modules use GitHub Classroom to distribute, manage, and submit
computational coursework. This is a trivial example which shows you how to
obtain and work with Git and GitHub to do your coursework.

Accepting the assignment
~~~~~~~~~~~~~~~~~~~~~~~~

For each GitHub Classroom assignment, your module will provide access to a link
that you can use to accept the assignment. In this case, there is a tiny toy
assignment created just for this exercise. `Accept the assignment by clicking
here <https://classroom.github.com/a/cChf4oeV>`_.

When you click on the assignment, if you're not already logged into your 


