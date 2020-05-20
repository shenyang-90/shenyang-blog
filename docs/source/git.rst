
Git
===

Basic Command
-------------

.. code::

   git status
   git add xxx(files / folder)
   git commit -m "xxx"
   git pull --rebase
   git push



Git Global Setup
----------------

.. code::

   git config --global user.name "xxxx"
   git config --global user.email "xxxx@xxxx.com"


Repository
----------


Create Repository
+++++++++++++++++

.. code::

   [/GIT]> git init --bare test.git
   [/home]> git clone /GIT/test.git
   [/home]> git add xxx
   [/home]> git add commit -m "xxx"
   [/home]> git branch --unset-upstream
   [/home]> git push --set-upstream origin master

.. note::

   Add `sharedRepository = 1` in `config` file.



Change Repository - New
+++++++++++++++++++++++

.. code::

   git init
   git remote add origin git@xxxx.git
   git add .
   git commit -m "Initial commit"
   git push -u origin master



Change Repository - Existing
++++++++++++++++++++++++++++

.. code::

   git remote rename origin old-origin
   git remote add origin git@xxxx.git
   git push -u origin --all
   git push -u origin --tags


.. code::

   git remote set-url origin git@xxxx.git



Brach
-----

New Brach
+++++++++

.. code::

   git checkout -b branch_a
   git push origin branch_a:branch_a


Existing Brach
++++++++++++++

.. code::

   git checkout -b local_branch origin/remote_branch
   git push origin remote_branch local_branch




Github / Gitlab with SSH Key
----------------------------

**Generate SSH Key**

.. code::

   ssh-keygen -t rsa -C "xxxx@xxxx.com"


The SSH Key is generated in ``~/.ssh/`` folder.


**Add SSH Key**

1. In Github / Gitlab, Settings -> SSH Key -> New SSH Key.
#. Copy ``~/.ssh/id_rsa.pub`` to Webpage.
