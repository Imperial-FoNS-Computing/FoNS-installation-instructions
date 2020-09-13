Git and GitHub Classroom
========================

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
------------

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
---------------

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
-------------------------

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
see below, 